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

# IDvbDefaultAuthorityDescriptor interface


## -description


Implements methods that get data from the default authority descriptor for a content reference identifier (CRID). 
The default authority descriptor is the first part of the CRID and identifies the body that created the CRID.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbDefaultAuthorityDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbDefaultAuthorityDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbDefaultAuthorityDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd615bd1-3db7-4577-aa10-d68ad61b068c">GetDefaultAuthority</a>
</td>
<td align="left" width="63%">
Gets the string identifying the default authority from a  DVB  CRID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9eb76e79-d7a3-419b-9c3e-6d4e16486ff3">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB  default authority descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d98d1a45-1d72-4142-8bb4-15ac4f738813">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB  default authority descriptor.

</td>
</tr>
</table> 

