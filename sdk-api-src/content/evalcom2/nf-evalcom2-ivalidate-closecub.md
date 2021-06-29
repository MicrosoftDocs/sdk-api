---
UID: NF:evalcom2.IValidate.CloseCUB
title: IValidate::CloseCUB (evalcom2.h)
description: The CloseCUB method closes an open Internal Consistency Evaluator (ICE) .cub file. Internal Consistency Evaluator (ICE) .cub files can be opened using the OpenCUB method.
helpviewer_keywords: ["CloseCUB","CloseCUB method","CloseCUB method","IValidate interface","IValidate interface","CloseCUB method","IValidate.CloseCUB","IValidate::CloseCUB","evalcom2/IValidate::CloseCUB","setup.ivalidate_closecub"]
old-location: setup\ivalidate_closecub.htm
tech.root: setup
ms.assetid: be0d21ee-bb15-4c6d-9d69-741adf047863
ms.date: 12/05/2018
ms.keywords: CloseCUB, CloseCUB method, CloseCUB method,IValidate interface, IValidate interface,CloseCUB method, IValidate.CloseCUB, IValidate::CloseCUB, evalcom2/IValidate::CloseCUB, setup.ivalidate_closecub
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
 - IValidate::CloseCUB
 - evalcom2/IValidate::CloseCUB
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
 - IValidate.CloseCUB
---

# IValidate::CloseCUB


## -description

The <b>CloseCUB</b> method closes an open <a href="/windows/desktop/Msi/internal-consistency-evaluators-ices">Internal Consistency Evaluator (ICE)</a> .cub file. Internal Consistency Evaluator (ICE) .cub files can be opened using the <a href="/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub">OpenCUB</a> method.



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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method failed. 

</td>
</tr>
</table>

## -remarks

The method returns S_FALSE if no .cub file has been opened using the <a href="/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub">OpenCUB</a> method.

## -see-also

<a href="/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate">IValidate</a>



<a href="/windows/desktop/Msi/using-evalcom2">Using Evalcom2</a>



<a href="/windows/desktop/Msi/validation-callback-functions">Validation Callback Functions</a>
