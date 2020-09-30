---
UID: NN:comsvcs.ISharedProperty
title: ISharedProperty (comsvcs.h)
description: Exposes property methods that you can use to set or retrieve the value of a shared property.
helpviewer_keywords: ["ISharedProperty","ISharedProperty interface [COM+]","ISharedProperty interface [COM+]","described","_cos_ISharedProperty_Interface","comsvcs/ISharedProperty","cos.isharedproperty"]
old-location: cos\isharedproperty.htm
tech.root: cos
ms.assetid: d3c3e888-fe08-4ea6-b94c-fdfcbe7fd08a
ms.date: 12/05/2018
ms.keywords: ISharedProperty, ISharedProperty interface [COM+], ISharedProperty interface [COM+],described, _cos_ISharedProperty_Interface, comsvcs/ISharedProperty, cos.isharedproperty
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISharedProperty
 - comsvcs/ISharedProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISharedProperty
---

# ISharedProperty interface


## -description

Exposes property methods that you can use to set or retrieve the value of a shared property. A shared property can contain any data type that can be represented by a <b>Variant</b>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISharedProperty</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISharedProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISharedProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-isharedproperty-get_value">get_Value</a>
</td>
<td align="left" width="63%">
Retrieves the value of a shared property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-isharedproperty-put_value">put_Value</a>
</td>
<td align="left" width="63%">
Sets the value of a shared property.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isharedpropertygroup">ISharedPropertyGroup</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isharedpropertygroupmanager">ISharedPropertyGroupManager</a>