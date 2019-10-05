---
UID: NN:dskquota.IDiskQuotaEvents
title: IDiskQuotaEvents (dskquota.h)
author: windows-sdk-content
description: Receives quota-related event notifications.
old-location: fs\idiskquotaevents.htm
tech.root: FileIO
ms.assetid: 4b5dcb1f-8edb-4fcb-94ea-2a627667071e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDiskQuotaEvents, IDiskQuotaEvents interface [Files], IDiskQuotaEvents interface [Files],described, _win32_idiskquotaevents, base.idiskquotaevents, dskquota/IDiskQuotaEvents, fs.idiskquotaevents
ms.topic: interface
f1_keywords: 
 - "dskquota/IDiskQuotaEvents"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiskQuotaEvents interface


## -description


A client must implement the 
<b>IDiskQuotaEvents</b> interface as an event sink that receives the quota-related event notifications. Its methods are called by the system whenever significant quota events have occurred. Currently, the only event supported is the asynchronous resolution of user account name information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiskQuotaEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDiskQuotaEvents</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/dskquota/nf-dskquota-idiskquotaevents-onusernamechanged">OnUserNameChanged</a>
</td>
<td align="left" width="63%">
Notifies the client's connection sink whenever a user's SID has been asynchronously resolved.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-interfaces">Disk Management Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/managing-disk-quotas">Disk Quotas</a>
 

 

