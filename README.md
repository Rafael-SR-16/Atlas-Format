# Atlas-Format

## Steps to follow:
1. Look in file_to_AnnData for the file format in which your single-cell data is stored.
2. Follow the instructions to store your data in AnnData format.
3. Conversion to AnnData is necessary to obtain the atlas format in this code.
4. An example table of the final data is shown.

### Conversion to AnnData available from:

- SCE
- CDS 
- Seurat
- Loom 
- HDF5 / H5
- AnnData / H5AD
- MTX 
- TSV / CSV (Text format)

## An Atlas-Format matrix requires:
1. Use a .txt file (see the attached example) where the first column lists official gene symbols, and subsequent columns contain counts corresponding to cell types/replicates.
2. Name each cell type at the top of its respective column exactly as you would like it to appear in the illustration.
3. We recommend representing each cell type with replicates (3–10) in consecutive columns, using exactly the same name at the top of each replicate column (without numbering each replicate).
4. Ideally, each replicate column should represent a real sub-cluster for a cell type, obtained through unsupervised methods. This ensures that variability in expression graphs reflects real data. Alternatively, replicates can be created by averaging supervised clusters.
5. Recomended normalize counts to CP10K for single-cell transcriptomics.
6. Use only two decimal places for counts.
7. For counts equal to 0, avoid additional characters (e.g., use "0" instead of "0.00"). This will help improve performance on the virtual machine.
