---
UID: NF:oleauto.SysFreeString
title: SysFreeString function (oleauto.h)
description: Deallocates a string allocated previously by SysAllocString, SysAllocStringByteLen, SysReAllocString, SysAllocStringLen, or SysReAllocStringLen.
helpviewer_keywords: ["SysFreeString","SysFreeString function [Automation]","_oa96_SysFreeString","automat.sysfreestring","oleauto/SysFreeString"]
old-location: automat\sysfreestring.htm
tech.root: automat
ms.assetid: 8f230ee3-5f6e-4cb9-a910-9c90b754dcd3
ms.date: 12/05/2018
ms.keywords: SysFreeString, SysFreeString function [Automation], _oa96_SysFreeString, automat.sysfreestring, oleauto/SysFreeString
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SysFreeString
 - oleauto/SysFreeString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SysFreeString
---

# SysFreeString function


## -description

Deallocates a string allocated previously by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>, <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstringbytelen">SysAllocStringByteLen</a>, <a href="/windows/desktop/api/oleauto/nf-oleauto-sysreallocstring">SysReAllocString</a>, <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstringlen">SysAllocStringLen</a>, or <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysreallocstringlen">SysReAllocStringLen</a>.

## -parameters

### -param bstrString [in, optional]

The previously allocated string. If this parameter is <b>NULL</b>, the function simply returns.