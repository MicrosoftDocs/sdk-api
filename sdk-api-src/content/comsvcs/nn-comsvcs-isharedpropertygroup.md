---
UID: NN:comsvcs.ISharedPropertyGroup
title: ISharedPropertyGroup
author: windows-sdk-content
description: Used to create and access the shared properties in a shared property group.
old-location: cos\isharedpropertygroup.htm
tech.root: cossdk
ms.assetid: e7f23c83-40d3-4b08-a185-cd6e3260e0a9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISharedPropertyGroup, ISharedPropertyGroup interface [COM+], ISharedPropertyGroup interface [COM+],described, _cos_ISharedPropertyGroup, comsvcs/ISharedPropertyGroup, cos.isharedpropertygroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# ISharedPropertyGroup interface


## -description


Used to create and access the shared properties in a shared property group.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISharedPropertyGroup</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ISharedPropertyGroup</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms686088(v=VS.85).aspx">CreateProperty</a>
</td>
<td align="left" width="63%">
Creates a new shared property with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681194(v=VS.85).aspx">CreatePropertyByPosition</a>
</td>
<td align="left" width="63%">
Creates a new shared property with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms688553(v=VS.85).aspx">get_Property</a>
</td>
<td align="left" width="63%">
Retrieves a reference to an existing shared property with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679198(v=VS.85).aspx">get_PropertyByPosition</a>
</td>
<td align="left" width="63%">
Retrieves a reference to an existing shared property with the specified index.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686759(v=VS.85).aspx">ISharedProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/ms682397(v=VS.85).aspx">ISharedPropertyGroupManager</a>
 

 

