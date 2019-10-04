---
UID: NF:shlwapi.SHSetThreadRef
title: SHSetThreadRef function (shlwapi.h)
author: windows-sdk-content
description: Stores a per-thread reference to a Component Object Model (COM) object. This allows the caller to control the thread's lifetime so that it can ensure that Windows won't shut down the thread before the caller is ready.
old-location: shell\SHSetThreadRef.htm
tech.root: shell
ms.assetid: 1d0d70ca-a0e6-4620-9a01-8d4986990b9c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SHSetThreadRef, SHSetThreadRef function [Windows Shell], _win32_SHSetThreadRef, shell.SHSetThreadRef, shlwapi/SHSetThreadRef
ms.topic: function
f1_keywords: 
 - "shlwapi/SHSetThreadRef"
dev_langs:
 - c++
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
 - SHSetThreadRef
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHSetThreadRef function


## -description


Stores a per-thread reference to a Component Object Model (COM) object. This allows the caller to control the thread's lifetime so that it can ensure that Windows won't shut down the thread before the caller is ready.


## -parameters




### -param punk [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the object for which you want to store a reference. This value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shgetthreadref">SHGetThreadRef</a> to retrieve the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shcreatethread">SHCreateThread</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shcreatethreadref">SHCreateThreadRef</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shgetthreadref">SHGetThreadRef</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shreleasethreadref">SHReleaseThreadRef</a>
 

 

