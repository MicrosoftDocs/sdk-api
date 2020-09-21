---
UID: NF:evalcom2.IValidate.OpenCUB
title: IValidate::OpenCUB (evalcom2.h)
description: The OpenCUB method opens an Internal Consistency Evaluator (ICE) file that is to be used for validation.
helpviewer_keywords: ["IValidate interface","OpenCUB method","IValidate.OpenCUB","IValidate::OpenCUB","OpenCUB","OpenCUB method","OpenCUB method","IValidate interface","evalcom2/IValidate::OpenCUB","setup.ivalidate_opencub"]
old-location: setup\ivalidate_opencub.htm
tech.root: setup
ms.assetid: cadf3c6e-6fbb-4d46-b9a8-4f2508f1e8bc
ms.date: 12/05/2018
ms.keywords: IValidate interface,OpenCUB method, IValidate.OpenCUB, IValidate::OpenCUB, OpenCUB, OpenCUB method, OpenCUB method,IValidate interface, evalcom2/IValidate::OpenCUB, setup.ivalidate_opencub
req.header: evalcom2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Evalcom2.dll version 3.0.3790.371 or later
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
req.lib: 
req.dll: Evalcom2.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IValidate::OpenCUB
 - evalcom2/IValidate::OpenCUB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Evalcom2.dll
api_name:
 - IValidate.OpenCUB
---

# IValidate::OpenCUB


## -description

The <b>OpenCUB</b> method opens an  <a href="/windows/desktop/Msi/internal-consistency-evaluators-ices">Internal Consistency Evaluator (ICE)</a> file that is to be used for validation.

## -parameters

### -param szCUBFile [in]

The fully qualified path to the <a href="/windows/desktop/Msi/internal-consistency-evaluators-ices">Internal Consistency Evaluator (ICE)</a> file to be used for validation.

## -returns

This method can return one of these values.

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
The method succeeded. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>szDatabase</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/Msi/internal-consistency-evaluators-ices">Internal Consistency Evaluator (ICE)</a> file typically has a .cub file name extension.

## -see-also

<a href="/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate">IValidate</a>



<a href="/windows/desktop/Msi/using-evalcom2">Using Evalcom2</a>



<a href="/windows/desktop/Msi/validation-callback-functions">Validation Callback Functions</a>