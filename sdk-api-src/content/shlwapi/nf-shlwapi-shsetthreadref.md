---
UID: NF:shlwapi.SHSetThreadRef
title: SHSetThreadRef function
author: windows-driver-content
description: Stores a per-thread reference to a Component Object Model (COM) object. This allows the caller to control the thread's lifetime so that it can ensure that Windows won't shut down the thread before the caller is ready.
old-location: shell\SHSetThreadRef.htm
old-project: shell
ms.assetid: 1d0d70ca-a0e6-4620-9a01-8d4986990b9c
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: SHSetThreadRef, SHSetThreadRef function [Windows Shell], _win32_SHSetThreadRef, shell.SHSetThreadRef, shlwapi/SHSetThreadRef
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
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	ShCore.dll
-	API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
-	API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
-	API-MS-Win-ShCore-thread-l1-1-0.dll
api_name:
-	SHSetThreadRef
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later); ShCore.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# SHSetThreadRef function


## -description


Stores a per-thread reference to a Component Object Model (COM) object. This allows the caller to control the thread's lifetime so that it can ensure that Windows won't shut down the thread before the caller is ready.


## -parameters




### -param punk [in, optional]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the object for which you want to store a reference. This value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use <a href="https://msdn.microsoft.com/307b284b-f493-4d24-a7be-17c150d62b34">SHGetThreadRef</a> to retrieve the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer.




## -see-also




<a href="https://msdn.microsoft.com/2140e396-29cd-4665-b684-337170570b73">SHCreateThread</a>



<a href="https://msdn.microsoft.com/6abca2df-832c-410b-93c7-5131e481e595">SHCreateThreadRef</a>



<a href="https://msdn.microsoft.com/307b284b-f493-4d24-a7be-17c150d62b34">SHGetThreadRef</a>



<a href="https://msdn.microsoft.com/7f3fd09b-baad-4019-a060-c68727aee61f">SHReleaseThreadRef</a>
 

 

