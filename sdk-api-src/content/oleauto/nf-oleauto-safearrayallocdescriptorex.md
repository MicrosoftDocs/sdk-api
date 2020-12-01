---
UID: NF:oleauto.SafeArrayAllocDescriptorEx
title: SafeArrayAllocDescriptorEx function (oleauto.h)
description: Creates a safe array descriptor for an array of any valid variant type, including VT_RECORD, without allocating the array data.
helpviewer_keywords: ["SafeArrayAllocDescriptorEx","SafeArrayAllocDescriptorEx function [Automation]","_oa96_SafeArrayAllocDescriptorEx","automat.safearrayallocdescriptorex","oleauto/SafeArrayAllocDescriptorEx"]
old-location: automat\safearrayallocdescriptorex.htm
tech.root: automat
ms.assetid: c368d278-ef62-4cf3-a7f8-c48549207c09
ms.date: 12/05/2018
ms.keywords: SafeArrayAllocDescriptorEx, SafeArrayAllocDescriptorEx function [Automation], _oa96_SafeArrayAllocDescriptorEx, automat.safearrayallocdescriptorex, oleauto/SafeArrayAllocDescriptorEx
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
 - SafeArrayAllocDescriptorEx
 - oleauto/SafeArrayAllocDescriptorEx
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
 - SafeArrayAllocDescriptorEx
---

# SafeArrayAllocDescriptorEx function


## -description

Creates a safe array descriptor for an array of any valid variant type, including VT_RECORD, without allocating the array data.

## -parameters

### -param vt [in]

The variant type.

### -param cDims [in]

The number of dimensions in the array.

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
</table>

## -remarks

Because <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayallocdescriptor">SafeArrayAllocDescriptor</a> does not take a VARTYPE, it is not possible to use it to create the safe array descriptor for an array of records. The <b>SafeArrayAllocDescriptorEx</b> is used to allocate a safe array descriptor for an array of records of the given dimensions.