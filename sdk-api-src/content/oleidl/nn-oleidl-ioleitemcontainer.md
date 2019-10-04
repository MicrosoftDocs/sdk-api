---
UID: NN:oleidl.IOleItemContainer
title: IOleItemContainer (oleidl.h)
author: windows-sdk-content
description: Used by item monikers when they are bound to the objects they identify.
old-location: com\ioleitemcontainer.htm
tech.root: com
ms.assetid: fe306a36-da24-4b1e-ab42-359d37962d36
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOleItemContainer, IOleItemContainer interface [COM], IOleItemContainer interface [COM],described, _com_ioleitemcontainer, com.ioleitemcontainer, oleidl/IOleItemContainer
ms.topic: interface
f1_keywords: 
 - "oleidl/IOleItemContainer"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobject">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the specified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-getobjectstorage">GetObjectStorage</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the storage for the specified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleitemcontainer-isrunning">IsRunning</a>
</td>
<td align="left" width="63%">
Determines whether the specified object is running.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-createitemmoniker">CreateItemMoniker</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>
 

 

