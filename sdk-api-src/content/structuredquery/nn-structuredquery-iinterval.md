---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IInterval interface


## -description


Provides a method to get the limits of an interval.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInterval</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInterval</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInterval</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/631f3ec2-cf8f-4c20-8933-c83bac4b3d58">GetLimits</a>
</td>
<td align="left" width="63%">
Specifies the lower and upper limits of an interval, each of which may be infinite or a specific value.
        


When a condition tree expresses that the value of a property must fall in a certain range, the property can be expressed as a leaf node. The node must be a <a href="_stg_propvariant">PROPVARIANT</a> containing a <b>vt</b> value type tag of VT_UNKNOWN and an IUnknown* <b>punkVal</b> that is a pointer to an object that implements <b>IInterval</b>.

</td>
</tr>
</table> 

