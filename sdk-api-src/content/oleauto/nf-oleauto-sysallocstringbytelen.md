---
UID: NF:oleauto.SysAllocStringByteLen
title: SysAllocStringByteLen function (oleauto.h)
description: Takes an ANSI string as input, and returns a BSTR that contains an ANSI string. Does not perform any ANSI-to-Unicode translation.
helpviewer_keywords: ["SysAllocStringByteLen","SysAllocStringByteLen function [Automation]","_oa96_SysAllocStringByteLen","automat.sysallocstringbytelen","oleauto/SysAllocStringByteLen"]
old-location: automat\sysallocstringbytelen.htm
tech.root: automat
ms.assetid: e7f49441-eff1-4c00-b61f-8522c4e250ef
ms.date: 12/05/2018
ms.keywords: SysAllocStringByteLen, SysAllocStringByteLen function [Automation], _oa96_SysAllocStringByteLen, automat.sysallocstringbytelen, oleauto/SysAllocStringByteLen
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
 - SysAllocStringByteLen
 - oleauto/SysAllocStringByteLen
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
 - SysAllocStringByteLen
---

# SysAllocStringByteLen function


## -description

Takes an ANSI string as input, and returns a BSTR that contains an ANSI string. Does not perform any ANSI-to-Unicode translation.

## -parameters

### -param psz [in, optional]

The string to copy, or NULL to keep the string uninitialized.

### -param len [in]

The number of bytes to copy. A null character is placed afterwards, allocating a total of <i>len</i> plus the size of <b>OLECHAR</b> bytes.

## -returns

A copy of the string, or NULL if there is insufficient memory to complete the operation.

## -remarks

This function is provided to create BSTRs that contain binary data. You can use this type of BSTR only in situations where it will not be translated from ANSI to Unicode, or vice versa. 

For example, do not use these BSTRs between a 16-bit and a 32-bit application running on a 32-bit Windows system. The OLE 16-bit to 32-bit (and 32-bit to 16-bit) interoperability layer will translate the BSTR and corrupt the binary data. The preferred method of passing binary data is to use a SAFEARRAY of VT_UI1, which will not be translated by OLE.

If psz is Null, a string of the requested length is allocated, but not initialized. The string psz can contain embedded null characters, and does not need to end with a Null. Free the returned string later with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

## -see-also

<a href="/previous-versions/windows/desktop/automat/string-manipulation-functions">String Manipulation Functions</a>