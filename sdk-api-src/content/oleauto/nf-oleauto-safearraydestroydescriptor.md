---
UID: NF:oleauto.SafeArrayDestroyDescriptor
title: SafeArrayDestroyDescriptor function (oleauto.h)
description: Destroys the descriptor of the specified safe array.
helpviewer_keywords: ["SafeArrayDestroyDescriptor","SafeArrayDestroyDescriptor function [Automation]","_oa96_SafeArrayDestroyDescriptor","automat.safearraydestroydescriptor","oleauto/SafeArrayDestroyDescriptor"]
old-location: automat\safearraydestroydescriptor.htm
tech.root: automat
ms.assetid: f1e8de45-673b-4f20-a639-18c724c82df1
ms.date: 12/05/2018
ms.keywords: SafeArrayDestroyDescriptor, SafeArrayDestroyDescriptor function [Automation], _oa96_SafeArrayDestroyDescriptor, automat.safearraydestroydescriptor, oleauto/SafeArrayDestroyDescriptor
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
 - SafeArrayDestroyDescriptor
 - oleauto/SafeArrayDestroyDescriptor
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
 - SafeArrayDestroyDescriptor
---

# SafeArrayDestroyDescriptor function


## -description

Destroys the descriptor of the specified safe array.

## -parameters

### -param psa [in]

A safe array descriptor.

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
<dt><b>DISP_E_ARRAYISLOCKED</b></dt>
</dl>
</td>
<td width="60%">
The array is locked.

</td>
</tr>
</table>

## -remarks

This function is typically used to destroy the descriptor of a safe array that contains elements with data types other than variants. Destroying the array descriptor does not destroy the elements in the array. Before destroying the array descriptor, call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraydestroydata">SafeArrayDestroyData</a> to free the elements.