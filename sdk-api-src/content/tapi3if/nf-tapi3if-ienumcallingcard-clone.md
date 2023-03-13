---
UID: NF:tapi3if.IEnumCallingCard.Clone
title: IEnumCallingCard::Clone (tapi3if.h)
description: The Clone method creates another enumerator that contains the same enumeration state as the current one. This method is hidden from Visual Basic and scripting languages. (IEnumCallingCard.Clone)
helpviewer_keywords: ["Clone","Clone method [TAPI 2.2]","Clone method [TAPI 2.2]","IEnumCallingCard interface","IEnumCallingCard interface [TAPI 2.2]","Clone method","IEnumCallingCard.Clone","IEnumCallingCard::Clone","_tapi3_ienumcallingcard_clone","tapi3.ienumcallingcard_clone","tapi3if/IEnumCallingCard::Clone"]
old-location: tapi3\ienumcallingcard_clone.htm
tech.root: tapi3
ms.assetid: fb1a2ac3-12d1-42f0-9c73-c4d0d8a88700
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumCallingCard interface, IEnumCallingCard interface [TAPI 2.2],Clone method, IEnumCallingCard.Clone, IEnumCallingCard::Clone, _tapi3_ienumcallingcard_clone, tapi3.ienumcallingcard_clone, tapi3if/IEnumCallingCard::Clone
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumCallingCard::Clone
 - tapi3if/IEnumCallingCard::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumCallingCard.Clone
---

# IEnumCallingCard::Clone


## -description

The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one. This method is hidden from Visual Basic and scripting languages.

## -parameters

### -param ppEnum [out]

Pointer to new 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard">IEnumCallingCard</a> interface.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnum</i> parameter not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Failed for unknown reasons.

</td>
</tr>
</table>

## -remarks

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard">IEnumCallingCard</a> interface returned by <b>IEnumCallingCard::Clone</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>IEnumCallingCard</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>
