---
UID: NF:shobjidl_core.SHResolveLibrary
title: SHResolveLibrary function
author: windows-sdk-content
description: Resolves all locations in a library, even those locations that have been moved or renamed.
old-location: shell\SHResolveLibrary.htm
old-project: shell
ms.assetid: a8730c09-f872-4bf8-9482-9dd5af31b509
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHResolveLibrary, SHResolveLibrary function [Windows Shell], _shell_SHResolveLibrary, shell.SHResolveLibrary, shobjidl_core/SHResolveLibrary
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
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
 - Windows.Storage.dll
api_name:
 - SHResolveLibrary
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SHResolveLibrary function


## -description


Resolves all locations in a library, even those locations that have been moved or renamed.


## -parameters




### -param psiLibrary [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object that represents the library.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function can block the calling thread for as long as it takes to resolve all the locations in the specified library. Because it blocks the thread from which it is called, it should not be called from a thread that also handles user interface interactions.

This function resolves all locations in the specified library in a single call. To resolve an individual location in a library, see the <a href="https://msdn.microsoft.com/f3d867a1-7396-4fba-87ea-45b02f86d681">IShellLibrary::ResolveFolder</a> method or the <a href="https://msdn.microsoft.com/e9c8aacd-9abb-4640-b9ed-1fa417d4d4cc">SHResolveFolderPathInLibrary</a> function.




## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/f3d867a1-7396-4fba-87ea-45b02f86d681">IShellLibrary::ResolveFolder</a>
 

 

