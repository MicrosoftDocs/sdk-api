---
UID: NF:bdaiface.IBDA_UserActivityService.SetCurrentTunerUseReason
title: IBDA_UserActivityService::SetCurrentTunerUseReason
author: windows-driver-content
description: Specifies the current tuner use reason for a Media Sink Device (MSD) in a Protected Broadcast Driver Architecture (PBDA) media graph.
old-location: mstv\ibda_useractivityservice_setcurrenttunerusereason.htm
old-project: mstv
ms.assetid: 248a0b01-02be-49b3-88ff-3b830d77e08d
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IBDA_UserActivityService interface [Microsoft TV Technologies],SetCurrentTunerUseReason method, IBDA_UserActivityService.SetCurrentTunerUseReason, IBDA_UserActivityService::SetCurrentTunerUseReason, SetCurrentTunerUseReason, SetCurrentTunerUseReason method [Microsoft TV Technologies], SetCurrentTunerUseReason method [Microsoft TV Technologies],IBDA_UserActivityService interface, bdaiface/IBDA_UserActivityService::SetCurrentTunerUseReason, mstv.ibda_useractivityservice_setcurrenttunerusereason
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_UserActivityService.SetCurrentTunerUseReason
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

