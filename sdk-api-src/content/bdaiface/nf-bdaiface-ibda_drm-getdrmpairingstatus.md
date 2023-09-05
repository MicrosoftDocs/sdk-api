---
UID: NF:bdaiface.IBDA_DRM.GetDRMPairingStatus
title: IBDA_DRM::GetDRMPairingStatus (bdaiface.h)
description: The GetDRMPairingStatus method queries the status of the DRM handshake.
helpviewer_keywords: ["GetDRMPairingStatus","GetDRMPairingStatus method [Microsoft TV Technologies]","GetDRMPairingStatus method [Microsoft TV Technologies]","IBDA_DRM interface","IBDA_DRM interface [Microsoft TV Technologies]","GetDRMPairingStatus method","IBDA_DRM.GetDRMPairingStatus","IBDA_DRM::GetDRMPairingStatus","IBDA_DRMGetDRMPairingStatus","bdaiface/IBDA_DRM::GetDRMPairingStatus","mstv.ibda_drm_getdrmpairingstatus"]
old-location: mstv\ibda_drm_getdrmpairingstatus.htm
tech.root: mstv
ms.assetid: dff38609-9e90-491c-b8c4-33fd07471895
ms.date: 12/05/2018
ms.keywords: GetDRMPairingStatus, GetDRMPairingStatus method [Microsoft TV Technologies], GetDRMPairingStatus method [Microsoft TV Technologies],IBDA_DRM interface, IBDA_DRM interface [Microsoft TV Technologies],GetDRMPairingStatus method, IBDA_DRM.GetDRMPairingStatus, IBDA_DRM::GetDRMPairingStatus, IBDA_DRMGetDRMPairingStatus, bdaiface/IBDA_DRM::GetDRMPairingStatus, mstv.ibda_drm_getdrmpairingstatus
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_DRM::GetDRMPairingStatus
 - bdaiface/IBDA_DRM::GetDRMPairingStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdaiface.h
api_name:
 - IBDA_DRM.GetDRMPairingStatus
---

# IBDA_DRM::GetDRMPairingStatus


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetDRMPairingStatus</b> method queries the status of the DRM handshake.

## -parameters

### -param pdwStatus [out]

Receives a value from the <a href="/windows/desktop/api/bdaiface/ne-bdaiface-bda_drmpairingerror">BDA_DrmPairingError</a> enumeration.

### -param phError [out]

Receives an <b>HRESULT</b> value indicating the success or failure of the DRM handshake.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The device does not support this functionality, or the handshake is still in progress.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_drm">IBDA_DRM Interface</a>