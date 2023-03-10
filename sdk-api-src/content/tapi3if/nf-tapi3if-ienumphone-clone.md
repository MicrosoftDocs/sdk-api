---
UID: NF:tapi3if.IEnumPhone.Clone
title: IEnumPhone::Clone (tapi3if.h)
description: The Clone method creates another enumerator that contains the same enumeration state as the current one. This method is hidden from Visual Basic and scripting languages. (IEnumPhone.Clone)
helpviewer_keywords: ["Clone","Clone method [TAPI 2.2]","Clone method [TAPI 2.2]","IEnumPhone interface","IEnumPhone interface [TAPI 2.2]","Clone method","IEnumPhone.Clone","IEnumPhone::Clone","_tapi3_ienumphone_clone","tapi3.ienumphone_clone","tapi3if/IEnumPhone::Clone"]
old-location: tapi3\ienumphone_clone.htm
tech.root: tapi3
ms.assetid: b55bb1f5-ecde-4565-97b6-29e79823b9cb
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumPhone interface, IEnumPhone interface [TAPI 2.2],Clone method, IEnumPhone.Clone, IEnumPhone::Clone, _tapi3_ienumphone_clone, tapi3.ienumphone_clone, tapi3if/IEnumPhone::Clone
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
 - IEnumPhone::Clone
 - tapi3if/IEnumPhone::Clone
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
 - IEnumPhone.Clone
---

# IEnumPhone::Clone


## -description

The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one. This method is hidden from Visual Basic and scripting languages.

## -parameters

### -param ppEnum [out]

Pointer to new 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone">IEnumPhone</a> interface.

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
The <i>ppEnum</i> parameter is not a valid pointer.

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
The method failed for unknown reasons.

</td>
</tr>
</table>

## -remarks

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone">IEnumPhone</a> interface returned by <b>IEnumPhone::Clone</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>IEnumPhone</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone">IEnumPhone</a>
