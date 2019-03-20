---
UID: NF:shobjidl_core.IShellLibrary.SaveInKnownFolder
title: IShellLibrary::SaveInKnownFolder (shobjidl_core.h)
author: windows-sdk-content
description: Saves the library to a new file in a specified known folder.
old-location: shell\IShellLibrary_SaveInKnownFolder.htm
tech.root: shell
ms.assetid: 3a6fa57f-808d-4893-a01c-f192355f8989
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IShellLibrary interface [Windows Shell],SaveInKnownFolder method, IShellLibrary.SaveInKnownFolder, IShellLibrary::SaveInKnownFolder, SaveInKnownFolder, SaveInKnownFolder method [Windows Shell], SaveInKnownFolder method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_SaveInKnownFolder, shell.IShellLibrary_SaveInKnownFolder, shobjidl_core/IShellLibrary::SaveInKnownFolder
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellLibrary.SaveInKnownFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellLibrary::SaveInKnownFolder


## -description


Saves the library to a new file in a specified known folder.
      


## -parameters




### -param kfidToSaveIn [in]

Type: <b>REFKNOWNFOLDERID</b>

The ID of the known folder in which to save the <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a> object.
               
               For more information, see <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a>.
               


### -param pszLibraryName [in]

Type: <b>LPCWSTR</b>

The file name under which to save the library. The file name must not include the file name extension; the file name extension is added automatically.


### -param lsf [in]

Type: <b><a href="https://msdn.microsoft.com/cae52226-0030-457b-aebf-00aaf860243d">LIBRARYSAVEFLAGS</a></b>

The <a href="https://msdn.microsoft.com/cae52226-0030-457b-aebf-00aaf860243d">LIBRARYSAVEFLAGS</a>  value that specifies how to handle a library name collision.


### -param ppsiSavedTo [out]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>**</b>

The <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object  that represents the library description file into    which the library was saved.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




<a href="https://msdn.microsoft.com/2a7de829-f0bc-4ace-aed4-83d0611ae292">IShellLibrary::Save</a> and <a href="https://msdn.microsoft.com/953b209b-fd18-49d0-84d3-ad9b815f2a3a">SHSaveLibraryInFolderPath</a> create a new library file, 
            and save the file to disk.
            
            To save changes made to a library that has an existing library file, call  <a href="https://msdn.microsoft.com/a340964d-ea20-4a3b-be8b-f4f4dbf624ed">IShellLibrary::Commit</a>.
         

If the library is saved in the Libraries known folder (FOLDERID_Libraries), the library's location is automatically added to the system index.
         




## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>



<a href="https://msdn.microsoft.com/12F6E6AE-2776-408c-B9AC-E885BE93C27F">Library Description Schema</a>



<a href="https://msdn.microsoft.com/953b209b-fd18-49d0-84d3-ad9b815f2a3a">SHSaveLibraryInFolderPath</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>
 

 

