---
UID: NF:bdaiface.IBDA_DRM.PerformDRMPairing
title: IBDA_DRM::PerformDRMPairing (bdaiface.h)
description: The PerformDRMPairing method requests the tuner to perform a DRM handshake with the user's computer.
helpviewer_keywords: ["IBDA_DRM interface [Microsoft TV Technologies]","PerformDRMPairing method","IBDA_DRM.PerformDRMPairing","IBDA_DRM::PerformDRMPairing","IBDA_DRMPerformDRMPairing","PerformDRMPairing","PerformDRMPairing method [Microsoft TV Technologies]","PerformDRMPairing method [Microsoft TV Technologies]","IBDA_DRM interface","bdaiface/IBDA_DRM::PerformDRMPairing","mstv.ibda_drm_performdrmpairing"]
old-location: mstv\ibda_drm_performdrmpairing.htm
tech.root: mstv
ms.assetid: a3cd9e0c-cfb1-445f-bafc-c1a4f24550f8
ms.date: 12/05/2018
ms.keywords: IBDA_DRM interface [Microsoft TV Technologies],PerformDRMPairing method, IBDA_DRM.PerformDRMPairing, IBDA_DRM::PerformDRMPairing, IBDA_DRMPerformDRMPairing, PerformDRMPairing, PerformDRMPairing method [Microsoft TV Technologies], PerformDRMPairing method [Microsoft TV Technologies],IBDA_DRM interface, bdaiface/IBDA_DRM::PerformDRMPairing, mstv.ibda_drm_performdrmpairing
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
 - IBDA_DRM::PerformDRMPairing
 - bdaiface/IBDA_DRM::PerformDRMPairing
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
 - IBDA_DRM.PerformDRMPairing
---

# IBDA_DRM::PerformDRMPairing


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>PerformDRMPairing</b> method requests the tuner to perform a DRM handshake with the user's computer.

## -parameters

### -param fSync [in]

If <b>TRUE</b>, the method blocks until the operation is completed. If <b>FALSE</b>, the operation is completed asynchronously.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

If you call this method asynchronously (<i>fSync</i> equal to <b>FALSE</b>), you can poll the status of the operation by calling <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_drm-getdrmpairingstatus">IBDA_DRM::GetDRMPairingStatus</a>. While the operation is in progress, <b>GetDRMPairingStatus</b> returns S_FALSE.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_drm">IBDA_DRM Interface</a>