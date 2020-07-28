---
UID: NF:shlwapi.SHCreateThreadRef
title: SHCreateThreadRef function (shlwapi.h)
description: Creates a per-thread reference to a Component Object Model (COM) object.
helpviewer_keywords: ["SHCreateThreadRef","SHCreateThreadRef function [Windows Shell]","_shell_SHCreateThreadRef","shell.SHCreateThreadRef","shlwapi/SHCreateThreadRef"]
old-location: shell\SHCreateThreadRef.htm
tech.root: shell
ms.assetid: 6abca2df-832c-410b-93c7-5131e481e595
ms.date: 12/05/2018
ms.keywords: SHCreateThreadRef, SHCreateThreadRef function [Windows Shell], _shell_SHCreateThreadRef, shell.SHCreateThreadRef, shlwapi/SHCreateThreadRef
f1_keywords:
- shlwapi/SHCreateThreadRef
dev_langs:
- c++
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

A pointer to a value, usually a local variable in the thread's <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)">ThreadProc</a>, that is used by the interface in <i>ppunk</i> as a reference counter.


### -param ppunk [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

The address of a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. If successful, this parameter holds the thread's <b>IUnknown</b> pointer on return. Your application is responsible for freeing the pointer when it is finished.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



See <a href="https://docs.microsoft.com/windows/desktop/shell/managing-thread-references">Managing Thread References</a> for more details on using the Shlwapi thread APIs.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shcreatethread">SHCreateThread</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shgetthreadref">SHGetThreadRef</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shreleasethreadref">SHReleaseThreadRef</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shsetthreadref">SHSetThreadRef</a>
 

 

