---
UID: NF:ctffunc.IEnumTfLatticeElements.Skip
title: IEnumTfLatticeElements::Skip (ctffunc.h)
description: IEnumTfLatticeElements::Skip method
helpviewer_keywords: ["IEnumTfLatticeElements interface [Text Services Framework]","Skip method","IEnumTfLatticeElements.Skip","IEnumTfLatticeElements::Skip","Skip","Skip method [Text Services Framework]","Skip method [Text Services Framework]","IEnumTfLatticeElements interface","_tsf_ienumtflatticeelements_skip_ref","ctffunc/IEnumTfLatticeElements::Skip","tsf.ienumtflatticeelements_skip"]
old-location: tsf\ienumtflatticeelements_skip.htm
tech.root: TSF
ms.assetid: 53dbe7f0-cc1f-4ba4-9ed5-7b328c707902
ms.date: 12/05/2018
ms.keywords: IEnumTfLatticeElements interface [Text Services Framework],Skip method, IEnumTfLatticeElements.Skip, IEnumTfLatticeElements::Skip, Skip, Skip method [Text Services Framework], Skip method [Text Services Framework],IEnumTfLatticeElements interface, _tsf_ienumtflatticeelements_skip_ref, ctffunc/IEnumTfLatticeElements::Skip, tsf.ienumtflatticeelements_skip
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Sptip.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - IEnumTfLatticeElements::Skip
 - ctffunc/IEnumTfLatticeElements::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sptip.dll
api_name:
 - IEnumTfLatticeElements.Skip
---

# IEnumTfLatticeElements::Skip


## -description

Moves the current position forward in the enumeration sequence by the specified number of elements.

## -parameters

### -param ulCount [in]

Contains the number of elements to skip.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method reached the end of the enumeration before the specified number of elements could be skipped.

</td>
</tr>
</table>

