# Git_EPIGIFT_Seurat_Compare

<br>

**Main goal**  
We want to assess if the EpiGIFT method (with the teta path) is accurate to extract significant genes between two conditions in terms of gene expression (scRNAseq data, number of mRNA per cell for each detected gene). We work with human CD34+ hematopoietic stem cells and 10XscRNAseq dataset. To do so, we will compare the list of significant genes between two conditions obtained with EpiGIFT with the ones we extract with the traditional method using the Seurat Package.    
  
**Working folder organization**  
- bin folder : contains the scripts (R, Rmd...)    
- data folder : contains raw data => DO NOT EXPORT ON GIT, ADD IT ON THE GITIGNORE FILE    
- report folder : contains html report from each script of the bin folder      
- exp folder : contains script's outputs (plots, tables...)      
- source codes to launch all scripts in the correct order      
- one or more README files  
- .gitignore file (hidden) : indicates which file should be saved on git when we "commit" our work  
  
**Scripts**  
  
*Part1 : EpiGIFT and theta path method* => Giota

- add a "tutorial" of the method with simple explanation of how it works and what we have as a result   - scRNAseq_EpiGIFT_Seurat_ThetaPath_ListGenes.Rmd  
 - put all your clean scripts for EpiGIFT method  
  
*Part2 : Seurat FindMarkers method* => Laëtitia => DONE
  
At first, we didn't know what was the optimal function to use to extract list of genes with Seurat function. Here are the investigations made to choose the optimal function. At the end, we decided to use the FindMarkers() function for the following analysis.  
- 1) scRNAseq_EpiGIFT_Seurat_InvestigationGenesSeurat.Rmd    
- 2) scRNAseq_EpiGIFT_Seurat_InvestigationGenesSeurat_GO.Rmd  
  
In this code, we use the FindMarkers() function from Seurat package to extract list of specific genes when we compare two conditions (ctrl cells VS drug cells). We did it for CTRL/DON, CTRL/2DG and CTRL/AOA. For later analysis, we choose to work first with CTRL/DON list of genes.  
- 3) scRNAseq_EpiGIFT_Seurat_FindMarkers_ListGenes.Rmd  
  
*Part3 : Compare list of genes from the two methods* => Giota and Laëtitia  

- 1) scRNAseq_EpiGIFT_Seurat_InvestigationCompare_Random.Rmd => add comments on EpiGIFT list
Definitive list of Fm => HERE => indicated in conclusion

- 2) scRNAseq_EpiGIFT_Seurat_InvestigationCompare_ThvalEpiGIFT.Rmd => add comments on EpiGIFT list + Conclusion
here we still have multiple lists for EpiGIFT.
why we don't have the same EpiGIFT lists between both code ? 

See at what moment we decided of a definitive list for EpiGift (write in a conclusion why we choose this one)
- 3) scRNAseq_EpiGIFT_Seurat_InvestigationCompare_ListGenes.Rmd : one list for EpiGIFT => I think we decided one final here 
=> save the common, onlyGIFT, onlyFM here 

- scRNAseq_EpiGIFT_Seurat_InvestigationCompare_GO_String.Rmd : One list for EpiGift  
- scRNAseq_EpiGIFT_Seurat_InvestigationCompare_pvalue.Rmd : One list for Epigift 
  
