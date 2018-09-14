---
UID: NN:oleidl.IOleItemContainer
title: IOleItemContainer
author: windows-sdk-content
description: Used by item monikers when they are bound to the objects they identify.
old-location: com\ioleitemcontainer.htm
tech.root: com
ms.assetid: fe306a36-da24-4b1e-ab42-359d37962d36
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IOleItemContainer, IOleItemContainer interface [COM], IOleItemContainer interface [COM],described, _com_ioleitemcontainer, com.ioleitemcontainer, oleidl/IOleItemContainer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.idl
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
 - OleIdl.h
api_name:
 - IOleItemContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleItemContainer interface


## -description


Used by item monikers when they are bound to the objects they identify. 


When any container of objects uses item monikers to identify its objects, it must define a naming scheme for those objects. The container's <b>IOleItemContainer</b> implementation uses knowledge of that naming scheme to retrieve an object given a particular name. Item monikers use the container's <b>IOleItemContainer</b> implementation during binding. 



This interface is not supported for use across machine boundaries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleItemContainer</b> interface inherits from <b>IOleContainer</b>. <b>IOleItemContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleItemContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08569037-7ecd-4e63-9f94-c2552c327800">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the specified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13a094bc-bacc-40d5-9682-ecc6072966fa">GetObjectStorage</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the storage for the specified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bbd7b58-b7ab-493e-8315-a35034ee2b7a">IsRunning</a>
</td>
<td align="left" width="63%">
Determines whether the specified object is running.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/339919ed-660c-4239-825b-7fa96c48e5cd">CreateItemMoniker</a>



<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>
 

 

