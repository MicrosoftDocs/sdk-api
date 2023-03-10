---
UID: NF:oleauto.SysStringByteLen
title: SysStringByteLen function (oleauto.h)
description: Returns the length (in bytes) of a BSTR.
helpviewer_keywords: ["SysStringByteLen","SysStringByteLen function [Automation]","_oa96_SysStringByteLen","automat.sysstringbytelen","oleauto/SysStringByteLen"]
old-location: automat\sysstringbytelen.htm
tech.root: automat
ms.assetid: 2a150503-f474-41b8-90dd-fbbc955bea99
ms.date: 12/05/2018
ms.keywords: SysStringByteLen, SysStringByteLen function [Automation], _oa96_SysStringByteLen, automat.sysstringbytelen, oleauto/SysStringByteLen
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
 - SysStringByteLen
 - oleauto/SysStringByteLen
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
 - SysStringByteLen
---

# SysStringByteLen function


## -description

Returns the length (in bytes) of a BSTR.

## -parameters

### -param bstr [in, optional]

A previously allocated string.

## -returns

The number of bytes in <i>bstr</i>, not including the terminating null character. If <i>bstr</i> is null the return value is zero.

## -remarks

The returned value may be different from <b>strlen</b>(bstr) if the BSTR contains embedded null characters. This function always returns the number of bytes specified in the len parameter of the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstringbytelen">SysAllocStringByteLen</a> function used to allocate the BSTR.

## -see-also

<a href="/previous-versions/windows/desktop/automat/string-manipulation-functions">String Manipulation Functions</a>