---
UID: NN:sdoias.ISdo
title: ISdo (sdoias.h)
description: Use the ISdo interface to store, retrieve, and update Server Data Objects (SDO) information.
helpviewer_keywords: ["ISdo","ISdo interface [Network Policy Server]","ISdo interface [Network Policy Server]","described","_sdo_isdo","nps.SDO_isdo","sdo.isdo","sdoias/ISdo"]
old-location: nps\SDO_isdo.htm
tech.root: Nps
ms.assetid: f8f49bf2-d8cc-40ad-ac52-05d74bcd931c
ms.date: 12/05/2018
ms.keywords: ISdo, ISdo interface [Network Policy Server], ISdo interface [Network Policy Server],described, _sdo_isdo, nps.SDO_isdo, sdo.isdo, sdoias/ISdo
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Iassdo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISdo
 - sdoias/ISdo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdo
---

# ISdo interface


## -description

Use the 
<b>ISdo</b> interface to store, retrieve, and update Server Data Objects (SDO) information.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISdo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISdo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISdo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-apply">Apply</a>
</td>
<td align="left" width="63%">
Writes changes to the datastore for the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-get__newenum">get_NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration interface for the object's properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-getpropertyinfo">GetPropertyInfo</a>
</td>
<td align="left" width="63%">
Retrieves an information interface for the specified property.

<b>Unsupported Interface:  </b>The <b>ISdoPropertyInfo</b> interface is unsupported and the use of this method to access it is discouraged.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty">PutProperty</a>
</td>
<td align="left" width="63%">
Sets the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-resetproperty">ResetProperty</a>
</td>
<td align="left" width="63%">
Resets the specified property to its default value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-restore">Restore</a>
</td>
<td align="left" width="63%">
Restores the values of the object's properties from the datastore.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/Nps/sdo-server-data-objects-interfaces">Server Data
    Objects Interfaces</a>



<a href="/windows/desktop/Nps/sdo-server-data-objects-reference">Server Data
    Objects Reference</a>