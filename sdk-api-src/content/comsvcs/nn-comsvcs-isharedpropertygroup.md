---
UID: NN:comsvcs.ISharedPropertyGroup
title: ISharedPropertyGroup (comsvcs.h)
author: windows-sdk-content
description: Used to create and access the shared properties in a shared property group.
old-location: cos\isharedpropertygroup.htm
tech.root: cossdk
ms.assetid: e7f23c83-40d3-4b08-a185-cd6e3260e0a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISharedPropertyGroup, ISharedPropertyGroup interface [COM+], ISharedPropertyGroup interface [COM+],described, _cos_ISharedPropertyGroup, comsvcs/ISharedPropertyGroup, cos.isharedpropertygroup
ms.topic: interface
f1_keywords: 
 - "comsvcs/ISharedPropertyGroup"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISharedPropertyGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISharedPropertyGroup interface


## -description


Used to create and access the shared properties in a shared property group.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISharedPropertyGroup</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISharedPropertyGroup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISharedPropertyGroup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isharedpropertygroup-createproperty">CreateProperty</a>
</td>
<td align="left" width="63%">
Creates a new shared property with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition">CreatePropertyByPosition</a>
</td>
<td align="left" width="63%">
Creates a new shared property with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isharedpropertygroup-get_property">get_Property</a>
</td>
<td align="left" width="63%">
Retrieves a reference to an existing shared property with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isharedpropertygroup-get_propertybyposition">get_PropertyByPosition</a>
</td>
<td align="left" width="63%">
Retrieves a reference to an existing shared property with the specified index.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-isharedproperty">ISharedProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-isharedpropertygroupmanager">ISharedPropertyGroupManager</a>
 

 

