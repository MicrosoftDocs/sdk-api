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

# IWSDOutboundAttachment interface


## -description


Enables applications to send attachment data in a message using a MIME container.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDOutboundAttachment</b> interface inherits from <a href="https://msdn.microsoft.com/9acbbca2-9b43-4bed-8917-be99f13fce13">IWSDAttachment</a>. <b>IWSDOutboundAttachment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDOutboundAttachment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/add0160c-bbf7-446e-8592-a05fd4d16fac">Abort</a>
</td>
<td align="left" width="63%">
Aborts the transfer of data on the attachment MIME data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Closes current attachment MIME data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a>
</td>
<td align="left" width="63%">
Sends attachment data to the remote host.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9acbbca2-9b43-4bed-8917-be99f13fce13">IWSDAttachment</a>
 

 

