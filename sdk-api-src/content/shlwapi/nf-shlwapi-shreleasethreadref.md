---
UID: NF:shlwapi.SHReleaseThreadRef
title: SHReleaseThreadRef function
author: windows-sdk-content
description: Releases a thread reference before the thread procedure returns.
old-location: shell\SHReleaseThreadRef.htm
old-project: shell
ms.assetid: 7f3fd09b-baad-4019-a060-c68727aee61f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SHReleaseThreadRef, SHReleaseThreadRef function [Windows Shell], _shell_SHReleaseThreadRef, shell.SHReleaseThreadRef, shlwapi/SHReleaseThreadRef
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: URL_SCHEME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-thread-l1-1-0.dll
api_name:
 - SHReleaseThreadRef
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# SHReleaseThreadRef function


## -description


Releases a thread reference before the thread procedure returns.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2140e396-29cd-4665-b684-337170570b73">SHCreateThread</a>



<a href="https://msdn.microsoft.com/6abca2df-832c-410b-93c7-5131e481e595">SHCreateThreadRef</a>



<a href="https://msdn.microsoft.com/307b284b-f493-4d24-a7be-17c150d62b34">SHGetThreadRef</a>



<a href="https://msdn.microsoft.com/1d0d70ca-a0e6-4620-9a01-8d4986990b9c">SHSetThreadRef</a>
 

 

