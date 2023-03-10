---
UID: NF:adhoc.IEnumDot11AdHocInterfaces.Clone
title: IEnumDot11AdHocInterfaces::Clone (adhoc.h)
description: Creates a new enumeration interface. (IEnumDot11AdHocInterfaces.Clone)
helpviewer_keywords: ["Clone","Clone method [NativeWIFI]","Clone method [NativeWIFI]","IEnumDot11AdHocInterfaces interface","IEnumDot11AdHocInterfaces interface [NativeWIFI]","Clone method","IEnumDot11AdHocInterfaces.Clone","IEnumDot11AdHocInterfaces::Clone","adhoc/IEnumDot11AdHocInterfaces::Clone","nwifi.ienumdot11adhocinterfaces_clone"]
old-location: nwifi\ienumdot11adhocinterfaces_clone.htm
tech.root: nwifi
ms.assetid: 3169ff1e-1994-4dd9-920d-c3f270f17b1c
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [NativeWIFI], Clone method [NativeWIFI],IEnumDot11AdHocInterfaces interface, IEnumDot11AdHocInterfaces interface [NativeWIFI],Clone method, IEnumDot11AdHocInterfaces.Clone, IEnumDot11AdHocInterfaces::Clone, adhoc/IEnumDot11AdHocInterfaces::Clone, nwifi.ienumdot11adhocinterfaces_clone
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
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
 - IEnumDot11AdHocInterfaces::Clone
 - adhoc/IEnumDot11AdHocInterfaces::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IEnumDot11AdHocInterfaces.Clone
---

# IEnumDot11AdHocInterfaces::Clone


## -description

Creates a new enumeration interface.

## -parameters

### -param ppEnum [out]

A pointer that, on successful return, points to an <a href="/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces">IEnumDot11AdHocInterfaces</a> interface.

## -returns

Possible return values include, but are not limited to, the following.

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
The method completed successfully.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
A specified interface is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces">IEnumDot11AdHocInterfaces</a>
