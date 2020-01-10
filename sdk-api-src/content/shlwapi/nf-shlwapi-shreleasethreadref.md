---
UID: NF:shlwapi.SHReleaseThreadRef
title: SHReleaseThreadRef function (shlwapi.h)
description: Releases a thread reference before the thread procedure returns.
old-location: shell\SHReleaseThreadRef.htm
tech.root: shell
ms.assetid: 7f3fd09b-baad-4019-a060-c68727aee61f
ms.date: 12/05/2018
ms.keywords: SHReleaseThreadRef, SHReleaseThreadRef function [Windows Shell], _shell_SHReleaseThreadRef, shell.SHReleaseThreadRef, shlwapi/SHReleaseThreadRef
f1_keywords:
- shlwapi/SHReleaseThreadRef
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHReleaseThreadRef function


## -description


Releases a thread reference before the thread procedure returns.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shcreatethread">SHCreateThread</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shcreatethreadref">SHCreateThreadRef</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shgetthreadref">SHGetThreadRef</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shsetthreadref">SHSetThreadRef</a>
 

 

