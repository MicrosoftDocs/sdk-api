---
UID: NF:oleauto.SysStringLen
title: SysStringLen function (oleauto.h)
description: Returns the length of a BSTR.
helpviewer_keywords: ["SysStringLen","SysStringLen function [Automation]","_oa96_SysStringLen","automat.sysstringlen","oleauto/SysStringLen"]
old-location: automat\sysstringlen.htm
tech.root: automat
ms.assetid: 65e792af-f8a8-4cdc-a279-494bba59394a
ms.date: 12/05/2018
ms.keywords: SysStringLen, SysStringLen function [Automation], _oa96_SysStringLen, automat.sysstringlen, oleauto/SysStringLen
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
 - SysStringLen
 - oleauto/SysStringLen
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
 - SysStringLen
---

# SysStringLen function


## -description

Returns the length of a BSTR.

## -parameters

### -param pbstr [in, optional]

A previously allocated string.

## -returns

The number of characters in <i>bstr</i>, not including the terminating null character. If <i>bstr</i> is null the return value is zero.

## -remarks

The returned value may be different from <b>strlen</b>(bstr) if the BSTR contains embedded Null characters. This function always returns the number of characters specified in the cch parameter of the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstringlen">SysAllocStringLen</a> function used to allocate the BSTR.

## -see-also

<a href="/previous-versions/windows/desktop/automat/string-manipulation-functions">String Manipulation Functions</a>