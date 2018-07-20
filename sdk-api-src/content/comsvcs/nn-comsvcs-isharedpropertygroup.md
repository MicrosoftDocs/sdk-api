---
UID: NN:comsvcs.ISharedPropertyGroup
title: ISharedPropertyGroup
author: windows-sdk-content
description: Used to create and access the shared properties in a shared property group.
old-location: cos\isharedpropertygroup.htm
old-project: cossdk
ms.assetid: e7f23c83-40d3-4b08-a185-cd6e3260e0a9
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ISharedPropertyGroup, ISharedPropertyGroup interface [COM+], ISharedPropertyGroup interface [COM+],described, _cos_ISharedPropertyGroup, comsvcs/ISharedPropertyGroup, cos.isharedpropertygroup
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
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
req.lib: 
req.dll: 
req.irql: 
---

# ISharedPropertyGroup interface


## -description


Used to create and access the shared properties in a shared property group.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISharedPropertyGroup</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ISharedPropertyGroup</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/bc34ec47-b39f-49fd-a8dd-8c96bb708e88">CreateProperty</a>
</td>
<td align="left" width="63%">
Creates a new shared property with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47e0e230-0952-4afb-a757-af387a7cddfb">CreatePropertyByPosition</a>
</td>
<td align="left" width="63%">
Creates a new shared property with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffbd82a8-35d5-4c9b-bf03-91f48dddc189">get_Property</a>
</td>
<td align="left" width="63%">
Retrieves a reference to an existing shared property with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/186cbf9f-a01b-4331-9f18-645d9e47f106">get_PropertyByPosition</a>
</td>
<td align="left" width="63%">
Retrieves a reference to an existing shared property with the specified index.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d3c3e888-fe08-4ea6-b94c-fdfcbe7fd08a">ISharedProperty</a>



<a href="https://msdn.microsoft.com/71c0a1de-5ea5-4496-b0e9-56d0cc8129a9">ISharedPropertyGroupManager</a>
 

 

