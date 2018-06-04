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

# IBDA_UserActivityService::SetCurrentTunerUseReason


## -description


Specifies the current tuner use reason for a Media Sink Device (MSD) in a Protected Broadcast Driver Architecture (PBDA) media graph. A <i>current tuner use reason</i>  records the reason that the MSD is currently using the tuner on a Media Transform Device (MTD).

 An MSD calls this method every time the current tuner use reason changes. For example, when an MSD starts a recording, it calls this method and sets the use reason as "user directed recording." An MSD must also call this method every time it sets a tuner device, even if the use reason has not changed.


## -parameters




### -param dwUseReason [in]

Specifies the tuner use reason. This is one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Setup or scanning

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Playback for a user

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Picture in Picture (PIP) playback for a user

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
User-directed recording

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Speculative recording

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2c8f14e-11d7-4385-a6c8-31b086ec1286">IBDA_UserActivityService</a>
 

 

