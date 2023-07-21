---
UID: NF:bdaiface.IBDA_UserActivityService.SetCurrentTunerUseReason
title: IBDA_UserActivityService::SetCurrentTunerUseReason (bdaiface.h)
description: Specifies the current tuner use reason for a Media Sink Device (MSD) in a Protected Broadcast Driver Architecture (PBDA) media graph.
helpviewer_keywords: ["IBDA_UserActivityService interface [Microsoft TV Technologies]","SetCurrentTunerUseReason method","IBDA_UserActivityService.SetCurrentTunerUseReason","IBDA_UserActivityService::SetCurrentTunerUseReason","SetCurrentTunerUseReason","SetCurrentTunerUseReason method [Microsoft TV Technologies]","SetCurrentTunerUseReason method [Microsoft TV Technologies]","IBDA_UserActivityService interface","bdaiface/IBDA_UserActivityService::SetCurrentTunerUseReason","mstv.ibda_useractivityservice_setcurrenttunerusereason"]
old-location: mstv\ibda_useractivityservice_setcurrenttunerusereason.htm
tech.root: mstv
ms.assetid: 248a0b01-02be-49b3-88ff-3b830d77e08d
ms.date: 12/05/2018
ms.keywords: IBDA_UserActivityService interface [Microsoft TV Technologies],SetCurrentTunerUseReason method, IBDA_UserActivityService.SetCurrentTunerUseReason, IBDA_UserActivityService::SetCurrentTunerUseReason, SetCurrentTunerUseReason, SetCurrentTunerUseReason method [Microsoft TV Technologies], SetCurrentTunerUseReason method [Microsoft TV Technologies],IBDA_UserActivityService interface, bdaiface/IBDA_UserActivityService::SetCurrentTunerUseReason, mstv.ibda_useractivityservice_setcurrenttunerusereason
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_UserActivityService::SetCurrentTunerUseReason
 - bdaiface/IBDA_UserActivityService::SetCurrentTunerUseReason
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_UserActivityService.SetCurrentTunerUseReason
---

# IBDA_UserActivityService::SetCurrentTunerUseReason


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_useractivityservice">IBDA_UserActivityService</a>