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

# IWindowsDriverUpdate2 interface


## -description


Contains the properties and methods that are available only from a Windows driver update.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsDriverUpdate2</b> interface inherits from <a href="https://msdn.microsoft.com/4e2eda04-4f86-4919-b754-dba90fa8d5d8">IWindowsDriverUpdate</a>. <b>IWindowsDriverUpdate2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWindowsDriverUpdate2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ad3f1bf-8da3-4d7d-8ed9-508422782861">CopyToCache</a>
</td>
<td align="left" width="63%">
Copies the external update binaries to an update.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsDriverUpdate2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6399d545-b300-4f78-b6df-c9892bc62fbb">CveIDs</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a collection of the Common Vulnerabilities and Exposures (CVE) identifiers that are associated with an update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn949436">IsPresent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether an update is installed on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/32c6982e-9654-4f8f-acca-ba1e4d52b210">RebootRequired</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the computer must be restarted after you install or uninstall an update.

</td>
</tr>
</table> 


## -remarks



This interface can be obtained by calling <a href="_com_iunknown_queryinterface">QueryInterface</a> method on an <a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a> interface only if the interface represents a Windows Driver update.




## -see-also




<a href="https://msdn.microsoft.com/4e2eda04-4f86-4919-b754-dba90fa8d5d8">IWindowsDriverUpdate</a>
 

 

