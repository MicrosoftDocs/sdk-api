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

# ITILSConfig interface


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ITILSConfig</b> interface allows configuration of the ILS directory. This interface is available only on Directory objects that return DT_ILS from 
<a href="https://msdn.microsoft.com/3f0ca4c2-4ba9-4a6e-877b-36486086368f">ITDirectory::get_DirectoryType</a>. The 
<b>ITILSConfig</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://msdn.microsoft.com/9ec8c0ed-2fed-4701-acb5-86b69c10f18c">ITDirectory</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITILSConfig</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITILSConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITILSConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7aa0a8e7-6799-4685-92a0-c2ce610d0e06">get_Port</a>
</td>
<td align="left" width="63%">
Gets the port number used to connect to the server of a given ILS directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d911a9c-6538-4919-9110-0425c53f91c4">put_Port</a>
</td>
<td align="left" width="63%">
Sets the port number used to connect to the server of a given ILS directory.

</td>
</tr>
</table> 

