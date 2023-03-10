---
UID: NF:oleauto.SafeArrayCopy
title: SafeArrayCopy function (oleauto.h)
description: Creates a copy of an existing safe array.
helpviewer_keywords: ["SafeArrayCopy","SafeArrayCopy function [Automation]","_oa96_SafeArrayCopy","automat.safearraycopy","oleauto/SafeArrayCopy"]
old-location: automat\safearraycopy.htm
tech.root: automat
ms.assetid: 8f84d4f6-1852-4ad8-b174-f3fa37e5bbd6
ms.date: 12/05/2018
ms.keywords: SafeArrayCopy, SafeArrayCopy function [Automation], _oa96_SafeArrayCopy, automat.safearraycopy, oleauto/SafeArrayCopy
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
 - SafeArrayCopy
 - oleauto/SafeArrayCopy
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
 - SafeArrayCopy
---

# SafeArrayCopy function


## -description

Creates a copy of an existing safe array.

## -parameters

### -param psa [in]

A safe array descriptor created by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreate">SafeArrayCreate</a>.

### -param ppsaOut [out]

The safe array descriptor.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument <i>psa</i> was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>

## -remarks

<b>SafeArrayCopy</b> calls the string or variant manipulation functions if the array to copy contains either of these data types. If the array being copied contains object references, the reference counts for the objects are incremented.

## -see-also

<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstringlen">SysAllocStringLen</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantcopy">VariantCopy</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantcopyind">VariantCopyInd</a>