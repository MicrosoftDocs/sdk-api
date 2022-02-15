---
UID: NE:bdaiface.BDA_DrmPairingError
title: BDA_DrmPairingError (bdaiface.h)
description: Specifies the status of a DRM handshake between a tuner and the user's computer.
helpviewer_keywords: ["BDA_DrmPairingError","BDA_DrmPairingError enumeration [Microsoft TV Technologies]","BDA_DrmPairing_DrmInitFailed","BDA_DrmPairing_DrmNotPaired","BDA_DrmPairing_DrmRePairSoon","BDA_DrmPairing_HardwareFailure","BDA_DrmPairing_NeedIndiv","BDA_DrmPairing_NeedRevocationData","BDA_DrmPairing_Other","BDA_DrmPairing_Succeeded","bdaiface/BDA_DrmPairingError","bdaiface/BDA_DrmPairing_DrmInitFailed","bdaiface/BDA_DrmPairing_DrmNotPaired","bdaiface/BDA_DrmPairing_DrmRePairSoon","bdaiface/BDA_DrmPairing_HardwareFailure","bdaiface/BDA_DrmPairing_NeedIndiv","bdaiface/BDA_DrmPairing_NeedRevocationData","bdaiface/BDA_DrmPairing_Other","bdaiface/BDA_DrmPairing_Succeeded","mstv.bda_drmpairingerror"]
old-location: mstv\bda_drmpairingerror.htm
tech.root: mstv
ms.assetid: d1b100e5-497e-4cb1-9cb8-38424c9eecf8
ms.date: 12/05/2018
ms.keywords: BDA_DrmPairingError, BDA_DrmPairingError enumeration [Microsoft TV Technologies], BDA_DrmPairing_DrmInitFailed, BDA_DrmPairing_DrmNotPaired, BDA_DrmPairing_DrmRePairSoon, BDA_DrmPairing_HardwareFailure, BDA_DrmPairing_NeedIndiv, BDA_DrmPairing_NeedRevocationData, BDA_DrmPairing_Other, BDA_DrmPairing_Succeeded, bdaiface/BDA_DrmPairingError, bdaiface/BDA_DrmPairing_DrmInitFailed, bdaiface/BDA_DrmPairing_DrmNotPaired, bdaiface/BDA_DrmPairing_DrmRePairSoon, bdaiface/BDA_DrmPairing_HardwareFailure, bdaiface/BDA_DrmPairing_NeedIndiv, bdaiface/BDA_DrmPairing_NeedRevocationData, bdaiface/BDA_DrmPairing_Other, bdaiface/BDA_DrmPairing_Succeeded, mstv.bda_drmpairingerror
req.header: bdaiface.h
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
targetos: Windows
req.typenames: BDA_DrmPairingError
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BDA_DrmPairingError
 - bdaiface/BDA_DrmPairingError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bdaiface.h
api_name:
 - BDA_DrmPairingError
---

# BDA_DrmPairingError enumeration


## -description

Specifies the status of a DRM handshake between a tuner and the user's computer.

## -enum-fields

### -field BDA_DrmPairing_Succeeded:0

The handshake was successful.

### -field BDA_DrmPairing_HardwareFailure

A hardware failure occurred.

### -field BDA_DrmPairing_NeedRevocationData

The tuner could not obtain the certificate revocation list.

### -field BDA_DrmPairing_NeedIndiv

The tuner could not perform individualization.

### -field BDA_DrmPairing_Other

Network interface (SCTE 55-1).

### -field BDA_DrmPairing_DrmInitFailed

The handshake failed during the initialization step.

### -field BDA_DrmPairing_DrmNotPaired

The client has not requested a handshake or the handshake is still in progress.

### -field BDA_DrmPairing_DrmRePairSoon

The handshake was successful but will soon time out. The client should refresh the handshake soon.

### -field BDA_DrmPairing_Aborted

### -field BDA_DrmPairing_NeedSDKUpdate

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-reference">BDA Reference</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_drm-getdrmpairingstatus">IBDA_DRM::GetDRMPairingStatus</a>
