---
UID: NF:shlwapi.SHSetThreadRef
title: SHSetThreadRef function (shlwapi.h)
description: Stores a per-thread reference to a Component Object Model (COM) object. This allows the caller to control the thread's lifetime so that it can ensure that Windows won't shut down the thread before the caller is ready.
helpviewer_keywords: ["SHSetThreadRef","SHSetThreadRef function [Windows Shell]","_win32_SHSetThreadRef","shell.SHSetThreadRef","shlwapi/SHSetThreadRef"]
old-location: shell\SHSetThreadRef.htm
tech.root: shell
ms.assetid: 1d0d70ca-a0e6-4620-9a01-8d4986990b9c
ms.date: 12/05/2018
ms.keywords: SHSetThreadRef, SHSetThreadRef function [Windows Shell], _win32_SHSetThreadRef, shell.SHSetThreadRef, shlwapi/SHSetThreadRef
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHSetThreadRef
 - shlwapi/SHSetThreadRef
dev_langs:
 - c++
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
---

# SHSetThreadRef function


## -description

Stores a per-thread reference to a Component Object Model (COM) object. This allows the caller to control the thread's lifetime so that it can ensure that Windows won't shut down the thread before the caller is ready.

## -parameters

### -param punk [in, optional]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the object for which you want to store a reference. This value can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shgetthreadref">SHGetThreadRef</a> to retrieve the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcreatethread">SHCreateThread</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcreatethreadref">SHCreateThreadRef</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shgetthreadref">SHGetThreadRef</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shreleasethreadref">SHReleaseThreadRef</a>