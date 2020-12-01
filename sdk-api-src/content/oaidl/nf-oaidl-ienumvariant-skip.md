---
UID: NF:oaidl.IEnumVARIANT.Skip
title: IEnumVARIANT::Skip (oaidl.h)
description: Attempts to skip over the next celt elements in the enumeration sequence.
helpviewer_keywords: ["IEnumVARIANT interface [Automation]","Skip method","IEnumVARIANT.Skip","IEnumVARIANT::Skip","Skip","Skip method [Automation]","Skip method [Automation]","IEnumVARIANT interface","_oa96_IEnumVARIANT::Skip","automat.ienumvariant_skip","oaidl/IEnumVARIANT::Skip"]
old-location: automat\ienumvariant_skip.htm
tech.root: automat
ms.assetid: 5fe6951f-1e21-4a3d-8694-96efb15e6d11
ms.date: 12/05/2018
ms.keywords: IEnumVARIANT interface [Automation],Skip method, IEnumVARIANT.Skip, IEnumVARIANT::Skip, Skip, Skip method [Automation], Skip method [Automation],IEnumVARIANT interface, _oa96_IEnumVARIANT::Skip, automat.ienumvariant_skip, oaidl/IEnumVARIANT::Skip
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumVARIANT::Skip
 - oaidl/IEnumVARIANT::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - stdole.dll
api_name:
 - IEnumVARIANT.Skip
---

# IEnumVARIANT::Skip


## -description

Attempts to skip over the next celt elements in the enumeration sequence.

## -parameters

### -param celt [in]

The number of elements to skip.

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
The specified number of elements was skipped.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The end of the sequence was reached before skipping the requested number of elements.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>