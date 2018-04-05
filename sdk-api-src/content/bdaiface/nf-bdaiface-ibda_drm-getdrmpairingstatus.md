---
UID: NF:bdaiface.IBDA_DRM.GetDRMPairingStatus
title: IBDA_DRM::GetDRMPairingStatus method
author: windows-driver-content
description: The GetDRMPairingStatus method queries the status of the DRM handshake.
old-location: mstv\ibda_drm_getdrmpairingstatus.htm
old-project: mstv
ms.assetid: dff38609-9e90-491c-b8c4-33fd07471895
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetDRMPairingStatus method [Microsoft TV Technologies], GetDRMPairingStatus method [Microsoft TV Technologies], IBDA_DRM interface, GetDRMPairingStatus,IBDA_DRM.GetDRMPairingStatus, IBDA_DRM, IBDA_DRM interface [Microsoft TV Technologies], GetDRMPairingStatus method, IBDA_DRM::GetDRMPairingStatus, IBDA_DRMGetDRMPairingStatus, bdaiface/IBDA_DRM::GetDRMPairingStatus, mstv.ibda_drm_getdrmpairingstatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bdaiface.h
api_name:
-	IBDA_DRM.GetDRMPairingStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_DRM::GetDRMPairingStatus method


## -description


The <b>GetDRMPairingStatus</b> method queries the status of the DRM handshake.


## -parameters




### -param pdwStatus [out]

Receives a value from the <a href="https://msdn.microsoft.com/d1b100e5-497e-4cb1-9cb8-38424c9eecf8">BDA_DrmPairingError</a> enumeration.


### -param phError






#### - phErrort [out]

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




<a href="https://msdn.microsoft.com/d0bde207-d550-4e98-85c7-b0d47b0cd637">IBDA_DRM Interface</a>
 

 

