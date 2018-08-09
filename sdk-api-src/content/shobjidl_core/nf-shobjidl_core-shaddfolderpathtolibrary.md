---
UID: NF:shobjidl_core.SHAddFolderPathToLibrary
title: SHAddFolderPathToLibrary function
author: windows-sdk-content
description: Adds a folder to a library.
old-location: shell\SHAddFolderPathToLibrary.htm
old-project: shell
ms.assetid: 308e7905-dfa1-438f-9e7e-f895517e7adb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SHAddFolderPathToLibrary, SHAddFolderPathToLibrary function [Windows Shell], _shell_SHAddFolderPathToLibrary, shell.SHAddFolderPathToLibrary, shobjidl_core/SHAddFolderPathToLibrary
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SHAddFolderPathToLibrary
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# SHAddFolderPathToLibrary function


## -description


Adds a folder to a library.


## -parameters




### -param plib [in]

Type: <b><a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a> object to which to add the folder.


### -param pszFolderPath [in]

Type: <b>PCWSTR</b>

The folder to add, specified by path.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is an inline helper function that wraps the <a href="https://msdn.microsoft.com/7455998a-56a8-4fc1-882b-c0942fd35d8c">IShellLibrary::AddFolder</a> method.




## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/7455998a-56a8-4fc1-882b-c0942fd35d8c">IShellLibrary::AddFolder</a>



<a href="https://msdn.microsoft.com/5dd2c197-8846-481f-b51e-ea0a93fd5e9b">IShellLibrary::LoadLibraryFromItem</a>



<a href="https://msdn.microsoft.com/3fc1147e-6338-4fec-b20d-db5eb1303fe1">IShellLibrary::LoadLibraryFromKnownFolder</a>



<a href="https://msdn.microsoft.com/2ba2c504-e96c-4b56-b2f2-196c0b74c9eb">IShellLibrary::RemoveFolder</a>



<a href="https://msdn.microsoft.com/9692f9d1-1504-43d0-9eb1-3759a8e2b42d">SHLoadLibraryFromItem</a>



<a href="https://msdn.microsoft.com/9486252b-9aaf-4daf-b307-5a5adddfaa99">SHLoadLibraryFromKnownFolder</a>



<a href="https://msdn.microsoft.com/49433938-d31e-49f8-9dc7-3df5fb3bfcad">SHLoadLibraryFromParsingName</a>



<a href="https://msdn.microsoft.com/34de407c-54f0-4be9-a383-4bf1baa63eef">SHRemoveFolderPathFromLibrary</a>
 

 

