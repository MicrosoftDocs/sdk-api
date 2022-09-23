---
UID: NF:tapi3if.IEnumPluggableSuperclassInfo.Clone
title: IEnumPluggableSuperclassInfo::Clone (tapi3if.h)
description: The Clone method creates another enumerator that contains the same enumeration state as the current one. This method is hidden from Visual Basic and scripting languages. (IEnumPluggableSuperclassInfo.Clone)
helpviewer_keywords: ["Clone","Clone method [TAPI 2.2]","Clone method [TAPI 2.2]","IEnumPluggableSuperclassInfo interface","IEnumPluggableSuperclassInfo interface [TAPI 2.2]","Clone method","IEnumPluggableSuperclassInfo.Clone","IEnumPluggableSuperclassInfo::Clone","_tapi3_ienumpluggablesuperclassinfo_clone","tapi3.ienumpluggablesuperclassinfo_clone","tapi3if/IEnumPluggableSuperclassInfo::Clone"]
old-location: tapi3\ienumpluggablesuperclassinfo_clone.htm
tech.root: tapi3
ms.assetid: ec56cac7-451b-4866-85cd-8a2dea12d1f5
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumPluggableSuperclassInfo interface, IEnumPluggableSuperclassInfo interface [TAPI 2.2],Clone method, IEnumPluggableSuperclassInfo.Clone, IEnumPluggableSuperclassInfo::Clone, _tapi3_ienumpluggablesuperclassinfo_clone, tapi3.ienumpluggablesuperclassinfo_clone, tapi3if/IEnumPluggableSuperclassInfo::Clone
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
 - IEnumPluggableSuperclassInfo::Clone
 - tapi3if/IEnumPluggableSuperclassInfo::Clone
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
 - IEnumPluggableSuperclassInfo.Clone
---

# IEnumPluggableSuperclassInfo::Clone


## -description

The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one. This method is hidden from Visual Basic and scripting languages.

## -parameters

### -param ppEnum [out]

Pointer to new 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo">IEnumPluggableSuperclassInfo</a> interface.

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
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo">IEnumPluggableSuperclassInfo</a> interface returned by <b>IEnumPluggableSuperclassInfo::Clone</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>IEnumPluggableSuperclassInfo</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo">IEnumPluggableSuperclassInfo</a>
