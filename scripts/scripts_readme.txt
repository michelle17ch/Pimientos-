#Este es el documento que contiene el script utilizado para realizar una filogenia 

1. Preparación de los datos 
# Descargar las secuencias en formato FASTA desde la NCBI 
# Realizar un alineamiento con el programa Muscle
#Navegar hasta el directorio de Muscle 
cd /path/to/muscle
# Ejecutar muscle 
./muscle -in input.fasta -out output.fasta
# Guardar el archivo formato FASTA

2. Realizar el árbol 
# Ejecutar IQTREE 
./iqtree2.exe -h
# Construcción del árbol 
# Ejecutar IQ-TREE con el archivo de alineamiento
./iqtree2.exe -s "$ALIGNMENT_FILE" -m MFP -bb 1000 -alrt 1000
# Verificar los archivos generados
echo "Archivos generados"

3. Consideraciones 
# Archivos generados importantes
Después de ejecutar el script, deberías ver varios archivos generados por IQ-TREE. Los más importantes son:
AlineamientoPimientos.treefile: Contiene el árbol filogenético.
AlineamientoPimientos.log: Contiene el registro del proceso de análisis.
Otros archivos pueden incluir detalles adicionales sobre el modelo y el bootstrap.

4. Visualización del árbol 
# Usar FigTree:
Descargar e instalar FigTree
Instálalo siguiendo las instrucciones para tu sistema operativo.
Abrir el archivo del árbol en FigTree:
Abrir FigTree.
En FigTree, selecciona File -> Open y navega hasta el archivo AlineamientoPimientos.treefile en la carpeta bin.
FigTree cargará y mostrará el árbol filogenético.
