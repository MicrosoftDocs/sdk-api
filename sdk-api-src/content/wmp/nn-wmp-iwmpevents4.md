---
UID: NN:wmp.IWMPEvents4
title: IWMPEvents4
author: windows-sdk-content
description: The IWMPEvents4 interface provides access to an event originating from the Windows Media Player 12 control so that an application that has this control embedded in it can respond to the event.
old-location: wmp\iwmpevents4.htm
tech.root: WMP
ms.assetid: b846ef23-1206-4a0b-866f-558b99b73f1d
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPEvents4, IWMPEvents4 interface [Windows Media Player], IWMPEvents4 interface [Windows Media Player],described, wmp.iwmpevents4, wmp/IWMPEvents4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmp.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPEvents4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents4 interface


## -description


The <a href="https://msdn.microsoft.com/654b7d78-97d4-4770-9729-dd1fed0431d9">IWMPEvents4</a> interface provides access to an event originating from the Windows Media Player 12 control so that an application that has this control embedded in it can respond to the event. The event exposed by <b>IWMPEvents4</b> is also exposed by the <a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPEvents4</b> interface inherits from <b>IWMPEvents3</b>. <b>IWMPEvents4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPEvents4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fb45a13-d82b-48b6-b9bb-46409f33a33f">SyncEstimationComplete</a>
</td>
<td align="left" width="63%">
Occurs when a size estimation, previously initiated by <a href="https://msdn.microsoft.com/49b07233-df9d-4fd0-836e-62b992408018">IWMPSyncDevice3::estimateSyncSize</a>, is complete.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5d9eb1c7-7022-4442-b67a-6a96fe5ce97f">Handling Events in C++</a>



<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>



<a href="https://msdn.microsoft.com/61cd0a2e-b94f-4c10-b3e2-ad1dc2a0b17d">IWMPEvents2 Interface</a>



<a href="https://msdn.microsoft.com/654b7d78-97d4-4770-9729-dd1fed0431d9">IWMPEvents3 Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 

