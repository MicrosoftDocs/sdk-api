---
UID: NF:shlwapi.SHReleaseThreadRef
title: SHReleaseThreadRef function (shlwapi.h)
description: Releases a thread reference before the thread procedure returns.
helpviewer_keywords: ["SHReleaseThreadRef","SHReleaseThreadRef function [Windows Shell]","_shell_SHReleaseThreadRef","shell.SHReleaseThreadRef","shlwapi/SHReleaseThreadRef"]
old-location: shell\SHReleaseThreadRef.htm
tech.root: shell
ms.assetid: 7f3fd09b-baad-4019-a060-c68727aee61f
ms.date: 12/05/2018
ms.keywords: SHReleaseThreadRef, SHReleaseThreadRef function [Windows Shell], _shell_SHReleaseThreadRef, shell.SHReleaseThreadRef, shlwapi/SHReleaseThreadRef
req.header: shlwapi.h
req.include-header: 
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
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHReleaseThreadRef
 - shlwapi/SHReleaseThreadRef
dev_langs:
 - c++
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
---

# SHReleaseThreadRef function


## -description

Releases a thread reference before the thread procedure returns.



## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcreatethread">SHCreateThread</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcreatethreadref">SHCreateThreadRef</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shgetthreadref">SHGetThreadRef</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shsetthreadref">SHSetThreadRef</a>
