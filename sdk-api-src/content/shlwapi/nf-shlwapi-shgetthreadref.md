---
UID: NF:shlwapi.SHGetThreadRef
title: SHGetThreadRef function (shlwapi.h)
description: Retrieves the per-thread object reference set by SHSetThreadRef.
helpviewer_keywords: ["SHGetThreadRef","SHGetThreadRef function [Windows Shell]","_win32_SHGetThreadRef","shell.SHGetThreadRef","shlwapi/SHGetThreadRef"]
old-location: shell\SHGetThreadRef.htm
tech.root: shell
ms.assetid: 307b284b-f493-4d24-a7be-17c150d62b34
ms.date: 12/05/2018
ms.keywords: SHGetThreadRef, SHGetThreadRef function [Windows Shell], _win32_SHGetThreadRef, shell.SHGetThreadRef, shlwapi/SHGetThreadRef
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
 - SHGetThreadRef
 - shlwapi/SHGetThreadRef
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
 - SHGetThreadRef
---

# SHGetThreadRef function


## -description

Retrieves the per-thread object reference set by <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shsetthreadref">SHSetThreadRef</a>.

## -parameters

### -param ppunk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

The address of a pointer that, when this function returns successfully, points to the object whose reference is stored. Your application is responsible for freeing this resource when it is no longer needed.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the object reference exists, or <b>E_NOINTERFACE</b> otherwise.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcreatethread">SHCreateThread</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcreatethreadref">SHCreateThreadRef</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shreleasethreadref">SHReleaseThreadRef</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shsetthreadref">SHSetThreadRef</a>