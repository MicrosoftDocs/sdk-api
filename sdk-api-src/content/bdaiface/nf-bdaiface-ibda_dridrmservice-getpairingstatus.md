---
UID: NF:bdaiface.IBDA_DRIDRMService.GetPairingStatus
title: IBDA_DRIDRMService::GetPairingStatus (bdaiface.h)
description: The GetPairingStatus method gets the Digital Rights Management (DRM) pairing status for a Media Transform Device (MTD) in a graph under the Protected Broadcast Driver Architecture (PBDA).
helpviewer_keywords: ["Green","Orange","Red","GetPairingStatus","GetPairingStatus method [DirectShow]","GetPairingStatus method [DirectShow]","IBDA_DRIDRMService interface","IBDA_DRIDRMService interface [DirectShow]","GetPairingStatus method","IBDA_DRIDRMService.GetPairingStatus","IBDA_DRIDRMService::GetPairingStatus","bdaiface/IBDA_DRIDRMService::GetPairingStatus","mstv.ibda_dridrmservice_getpairingstatus"]
old-location: mstv\ibda_dridrmservice_getpairingstatus.htm
tech.root: mstv
ms.assetid: 01918e99-17e6-4c24-bb85-ba71cf68cf09
ms.date: 12/05/2018
ms.keywords: Green, Orange, Red, GetPairingStatus, "GetPairingStatus method [DirectShow]", "GetPairingStatus method [DirectShow]", IBDA_DRIDRMService interface, "IBDA_DRIDRMService interface [DirectShow]", GetPairingStatus method, IBDA_DRIDRMService.GetPairingStatus, IBDA_DRIDRMService::GetPairingStatus, bdaiface/IBDA_DRIDRMService::GetPairingStatus, mstv.ibda_dridrmservice_getpairingstatus
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
 - IBDA_DRIDRMService::GetPairingStatus
 - bdaiface/IBDA_DRIDRMService::GetPairingStatus
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
 - IBDA_DRIDRMService.GetPairingStatus
---

# IBDA_DRIDRMService::GetPairingStatus


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetPairingStatus</b> method gets the Digital Rights Management (DRM) pairing status for a Media Transform Device (MTD) in a graph under the Protected Broadcast Driver Architecture (PBDA). This status indicates whether a secure pairing exists between the MTD and a Media Sink Device (MSD) so that controlled-access (CA) content can be released.

## -parameters

### -param penumPairingStatus [in, out]

Address of a variable that gets the pairing device status. The caller passes in a pointer to this variable, and this method returns the correct status value in this parameter. The pairing status that is passed back  can be any of the following values:
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="_Green_"></a><a id="_green_"></a><a id="_GREEN_"></a><dl>
<dt><b>"Green"</b></dt>
</dl>
</td>
<td width="60%">
The MTD is paired with an MSD, so CA content is released under DRM protection.

</td>
</tr>
<tr>
<td width="40%"><a id="_Orange_"></a><a id="_orange_"></a><a id="_ORANGE_"></a><dl>
<dt><b>"Orange"</b></dt>
</dl>
</td>
<td width="60%">
The MTD is paired with an MSD, but this pairing is about to time out. The MSD is expected to refresh its pairing in the background. CA content is released under DRM protection.

</td>
</tr>
<tr>
<td width="40%"><a id="_Red_"></a><a id="_red_"></a><a id="_RED_"></a><dl>
<dt><b>"Red"</b></dt>
</dl>
</td>
<td width="60%">
The MTD is not paired with an MSD, so CA content is is not released.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_dridrmservice">IBDA_DRIDRMService</a>