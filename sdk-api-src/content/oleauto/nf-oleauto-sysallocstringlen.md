---
UID: NF:oleauto.SysAllocStringLen
title: SysAllocStringLen function (oleauto.h)
description: Allocates a new string, copies the specified number of characters from the passed string, and appends a null-terminating character.
helpviewer_keywords: ["SysAllocStringLen","SysAllocStringLen function [Automation]","_oa96_SysAllocStringLen","automat.sysallocstringlen","oleauto/SysAllocStringLen"]
old-location: automat\sysallocstringlen.htm
tech.root: automat
ms.assetid: f98bff39-bc5f-4a81-85d7-d5228e20fbc8
ms.date: 12/05/2018
ms.keywords: SysAllocStringLen, SysAllocStringLen function [Automation], _oa96_SysAllocStringLen, automat.sysallocstringlen, oleauto/SysAllocStringLen
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
 - SysAllocStringLen
 - oleauto/SysAllocStringLen
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
 - SysAllocStringLen
---

# SysAllocStringLen function


## -description

Allocates a new string, copies the specified number of characters from the passed string, and appends a null-terminating character.

## -parameters

### -param strIn [in]

The input string.

### -param ui [in]

The number of characters to copy. A null character is placed afterwards, allocating a total of <i>ui</i> plus one characters.

## -returns

A copy of the string, or <b>NULL</b> if there is insufficient memory to complete the operation.

## -remarks

The string can contain embedded null characters and does not need to end with a <b>NULL</b>. Free the returned string later with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>. If <i>strIn</i> is not <b>NULL</b>, then the memory allocated to <i>strIn</i> must be at least <i>ui</i> characters long.

<div class="alert"><b>Note</b>  This function does not convert a <b>char *</b> string into a Unicode <b>BSTR</b>.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/automat/string-manipulation-functions">String Manipulation Functions</a>