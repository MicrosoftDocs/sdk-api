---
UID: NF:shlwapi.SHCreateThreadRef
title: SHCreateThreadRef function (shlwapi.h)
author: windows-sdk-content
description: Creates a per-thread reference to a Component Object Model (COM) object.
old-location: shell\SHCreateThreadRef.htm
tech.root: shell
ms.assetid: 6abca2df-832c-410b-93c7-5131e481e595
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SHCreateThreadRef, SHCreateThreadRef function [Windows Shell], _shell_SHCreateThreadRef, shell.SHCreateThreadRef, shlwapi/SHCreateThreadRef
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 6.0 or later)
req.irql: 
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
 - SHCreateThreadRef
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHCreateThreadRef function


## -description


Creates a per-thread reference to a Component Object Model (COM) object.


## -parameters




### -param pcRef [in]

Type: <b>LONG*</b>

A pointer to a value, usually a local variable in the thread's <a href="https://msdn.microsoft.com/f0dc203f-200e-42f1-940c-24e3fe080175">ThreadProc</a>, that is used by the interface in <i>ppunk</i> as a reference counter.


### -param ppunk [out]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

The address of a pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. If successful, this parameter holds the thread's <b>IUnknown</b> pointer on return. Your application is responsible for freeing the pointer when it is finished.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



See <a href="https://msdn.microsoft.com/d8d479fd-c45a-4dfa-b496-76abc7c09a42">Managing Thread References</a> for more details on using the Shlwapi thread APIs.




## -see-also




<a href="https://msdn.microsoft.com/2140e396-29cd-4665-b684-337170570b73">SHCreateThread</a>



<a href="https://msdn.microsoft.com/307b284b-f493-4d24-a7be-17c150d62b34">SHGetThreadRef</a>



<a href="https://msdn.microsoft.com/7f3fd09b-baad-4019-a060-c68727aee61f">SHReleaseThreadRef</a>



<a href="https://msdn.microsoft.com/1d0d70ca-a0e6-4620-9a01-8d4986990b9c">SHSetThreadRef</a>
 

 

