---
UID: NF:oleauto.SafeArrayCopyData
title: SafeArrayCopyData function (oleauto.h)
description: Copies the source array to the specified target array after releasing any resources in the target array.
helpviewer_keywords: ["SafeArrayCopyData","SafeArrayCopyData function [Automation]","_oa96_SafeArrayCopyData","automat.safearraycopydata","oleauto/SafeArrayCopyData"]
old-location: automat\safearraycopydata.htm
tech.root: automat
ms.assetid: 32c1fc4f-3fe0-490f-b5af-640514a8cecc
ms.date: 12/05/2018
ms.keywords: SafeArrayCopyData, SafeArrayCopyData function [Automation], _oa96_SafeArrayCopyData, automat.safearraycopydata, oleauto/SafeArrayCopyData
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
 - SafeArrayCopyData
 - oleauto/SafeArrayCopyData
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
 - SafeArrayCopyData
---

# SafeArrayCopyData function


## -description

Copies the source array to the specified target array after releasing any resources in the target array. This is similar to <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycopy">SafeArrayCopy</a>, except that the target array has to be set up by the caller. The target is not allocated or reallocated.

## -parameters

### -param psaSource [in]

The safe array to copy.

### -param psaTarget [in]

The target safe array.

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