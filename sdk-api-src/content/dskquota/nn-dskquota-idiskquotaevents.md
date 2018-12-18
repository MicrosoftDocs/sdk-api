---
UID: NN:dskquota.IDiskQuotaEvents
title: IDiskQuotaEvents
author: windows-sdk-content
description: Receives quota-related event notifications.
old-location: fs\idiskquotaevents.htm
tech.root: fileio
ms.assetid: 4b5dcb1f-8edb-4fcb-94ea-2a627667071e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiskQuotaEvents, IDiskQuotaEvents interface [Files], IDiskQuotaEvents interface [Files],described, _win32_idiskquotaevents, base.idiskquotaevents, dskquota/IDiskQuotaEvents, fs.idiskquotaevents
ms.topic: interface
req.header: dskquota.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Dskquota.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dskquota.dll
api_name:
 - IDiskQuotaEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiskQuotaEvents interface


## -description


A client must implement the 
<b>IDiskQuotaEvents</b> interface as an event sink that receives the quota-related event notifications. Its methods are called by the system whenever significant quota events have occurred. Currently, the only event supported is the asynchronous resolution of user account name information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiskQuotaEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDiskQuotaEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiskQuotaEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d01cb679-03e2-4b76-b068-f64e576709fb">OnUserNameChanged</a>
</td>
<td align="left" width="63%">
Notifies the client's connection sink whenever a user's SID has been asynchronously resolved.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c1f79e2e-834b-41dc-a15f-6dd1034d021b">Disk Management Interfaces</a>



<a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">Disk Quotas</a>
 

 

