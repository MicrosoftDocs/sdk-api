---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

