import os
import shutil
import Metashape


def main():
 
  dest_path = Metashape.app.getExistingDirectory("Export assets to folder:")
  doc = Metashape.app.document
  chunk = doc.chunk
  print ("Exporting cameras ...")
  for camera in chunk.cameras:
    print (camera.photo.path)
    shutil.copy2(camera.photo.path, dest_path)
   
  print("Script finished. Assets exported to " + dest_path + "\n")

Metashape.app.addMenuItem("Custom menu/Export Assets", main)
