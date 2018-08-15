---
UID: NF:shobjidl.SHResolveFolderPathInLibrary
title: SHResolveFolderPathInLibrary function
author: windows-sdk-content
description: Attempts to resolve the target location of a library folder that has been moved or renamed.
old-location: shell\SHResolveFolderPathInLibrary.htm
old-project: shell
ms.assetid: e9c8aacd-9abb-4640-b9ed-1fa417d4d4cc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SHResolveFolderPathInLibrary, SHResolveFolderPathInLibrary function [Windows Shell], _shell_SHResolveFolderPathInLibrary, shell.SHResolveFolderPathInLibrary, shobjidl/SHResolveFolderPathInLibrary
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shobjidl.h
req.include-header: 
req.redist: 
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
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl.h
api_name:
 - SHResolveFolderPathInLibrary
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# SHResolveFolderPathInLibrary function


## -description


Attempts to resolve the target location of a library folder that has been moved or renamed.


## -parameters




### -param plib [in]

Type: <b><a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>*</b>

The <a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a> object for which to resolve the target location.


### -param pszFolderPath [in]

Type: <b>PCWSTR</b>

The path of the library folder to locate.


### -param dwTimeout [in]

Type: <b>DWORD</b>

The maximum time, in milliseconds, that the method attempts to locate the folder before returning. If the folder could not be located before the specified time elapses, an error is returned.


### -param ppszResolvedPath [out]

Type: <b>PWSTR*</b>

A pointer to a string that, when this function successfully returns, contains the current path of the library folder specified in <i>plib</i>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is an inline helper function that wraps the <a href="https://msdn.microsoft.com/f3d867a1-7396-4fba-87ea-45b02f86d681">IShellLibrary::ResolveFolder</a> method.




## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/f3d867a1-7396-4fba-87ea-45b02f86d681">IShellLibrary::ResolveFolder</a>
 

 

