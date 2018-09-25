---
UID: NF:shlwapi.SHGetThreadRef
title: SHGetThreadRef function
author: windows-sdk-content
description: Retrieves the per-thread object reference set by SHSetThreadRef.
old-location: shell\SHGetThreadRef.htm
tech.root: shell
ms.assetid: 307b284b-f493-4d24-a7be-17c150d62b34
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: SHGetThreadRef, SHGetThreadRef function [Windows Shell], _win32_SHGetThreadRef, shell.SHGetThreadRef, shlwapi/SHGetThreadRef
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later); ShCore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-thread-l1-1-0.dll
api_name:
 - SHGetThreadRef
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHGetThreadRef function


## -description


Retrieves the per-thread object reference set by <a href="https://msdn.microsoft.com/1d0d70ca-a0e6-4620-9a01-8d4986990b9c">SHSetThreadRef</a>.


## -parameters




### -param ppunk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

The address of a pointer that, when this function returns successfully, points to the object whose reference is stored. Your application is responsible for freeing this resource when it is no longer needed.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the object reference exists, or <b>E_NOINTERFACE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/2140e396-29cd-4665-b684-337170570b73">SHCreateThread</a>



<a href="https://msdn.microsoft.com/6abca2df-832c-410b-93c7-5131e481e595">SHCreateThreadRef</a>



<a href="https://msdn.microsoft.com/7f3fd09b-baad-4019-a060-c68727aee61f">SHReleaseThreadRef</a>



<a href="https://msdn.microsoft.com/1d0d70ca-a0e6-4620-9a01-8d4986990b9c">SHSetThreadRef</a>
 

 

