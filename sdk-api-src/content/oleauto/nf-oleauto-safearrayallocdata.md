---
UID: NF:oleauto.SafeArrayAllocData
title: SafeArrayAllocData function (oleauto.h)
description: Allocates memory for a safe array, based on a descriptor created with SafeArrayAllocDescriptor.
helpviewer_keywords: ["SafeArrayAllocData","SafeArrayAllocData function [Automation]","_oa96_SafeArrayAllocData","automat.safearrayallocdata","oleauto/SafeArrayAllocData"]
old-location: automat\safearrayallocdata.htm
tech.root: automat
ms.assetid: a1f984cd-9638-415d-8582-25b1bdfbd694
ms.date: 12/05/2018
ms.keywords: SafeArrayAllocData, SafeArrayAllocData function [Automation], _oa96_SafeArrayAllocData, automat.safearrayallocdata, oleauto/SafeArrayAllocData
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
 - SafeArrayAllocData
 - oleauto/SafeArrayAllocData
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
 - SafeArrayAllocData
---

# SafeArrayAllocData function


## -description

Allocates memory for a safe array, based on a descriptor created with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayallocdescriptor">SafeArrayAllocDescriptor</a>.

## -parameters

### -param psa [in]

A safe array descriptor created by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayallocdescriptor">SafeArrayAllocDescriptor</a>.

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
The argument <i>psa</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The array could not be locked.

</td>
</tr>
</table>