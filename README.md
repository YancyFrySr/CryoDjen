# CryoDjen
# for Working With PE, Adapted some code i found to learn about objects so if anythings wrong please let me know
# 
###########
#Basic Use#
###########

##include <iostream>
#include<stdio.h>
#include <tchar.h>
#include "PELibber.h"

int main(int argc, char* argv[]) {
	char* filename = argv[1];
	PE_File_Loader currentFile(filename);
	std::cout << "\n\nEnd" << std::endl;
	system("PAUSE");
	printf("\n[-] Section Test\n=============================================================\n");

	std::vector<Section_Loader> sections;
	sections = currentFile.getSectionObjects();
	
	int numberOfSectionObjects = currentFile.getNumSections();
	
	for ( int j = 0; j < numberOfSectionObjects; j++ )
		sections[ j ].dumpSectionInfo();

	printf("\n[-] Section Test Completed!\n=============================================================\n");

	system("PAUSE");
	return 0;
}

