---
UID: NF:shobjidl_core.SHSaveLibraryInFolderPath
title: SHSaveLibraryInFolderPath function
author: windows-sdk-content
description: Saves an IShellLibrary object to disk.
old-location: shell\SHSaveLibraryInFolderPath.htm
tech.root: shell
ms.assetid: 953b209b-fd18-49d0-84d3-ad9b815f2a3a
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: SHSaveLibraryInFolderPath, SHSaveLibraryInFolderPath function [Windows Shell], _shell_SHSaveLibraryInFolderPath, shell.SHSaveLibraryInFolderPath, shobjidl_core/SHSaveLibraryInFolderPath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SHSaveLibraryInFolderPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHSaveLibraryInFolderPath function


## -description


Saves an <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a> object to disk.


## -parameters




### -param plib [in]

Type: <b><a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a> object to save.


### -param pszFolderPath [in]

Type: <b>PCWSTR</b>

A pointer to the path to the folder in which to save the library.


### -param pszLibraryName [in]

Type: <b>PCWSTR</b>

A pointer to a file name under which to save the library. The file name must not include the file name extension. The file name extension is added automatically.


### -param lsf [in]

Type: <b><a href="https://msdn.microsoft.com/cae52226-0030-457b-aebf-00aaf860243d">LIBRARYSAVEFLAGS</a></b>

A value from the <a href="https://msdn.microsoft.com/cae52226-0030-457b-aebf-00aaf860243d">LIBRARYSAVEFLAGS</a> enumeration that specifies how to handle a library name collision.


### -param ppszSavedToPath [out, optional]

Type: <b>PWSTR*</b>

A pointer to a string that, when this function returns successfully, receives the path to the library description file into which the library was saved. If this path is not required, the value of this parameter can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is an inline helper function that wraps the <a href="https://msdn.microsoft.com/2a7de829-f0bc-4ace-aed4-83d0611ae292">IShellLibrary::Save</a> method.




## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/2a7de829-f0bc-4ace-aed4-83d0611ae292">IShellLibrary::Save</a>



<a href="https://msdn.microsoft.com/3a6fa57f-808d-4893-a01c-f192355f8989">IShellLibrary::SaveInKnownFolder</a>
 

 

