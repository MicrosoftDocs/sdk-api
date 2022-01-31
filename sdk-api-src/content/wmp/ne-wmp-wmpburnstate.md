---
UID: NE:wmp.WMPBurnState
title: WMPBurnState (wmp.h)
description: The WMPBurnState enumeration type defines the possible operational states of Windows Media Player as it burns a CD.
helpviewer_keywords: ["WMPBurnState","WMPBurnState enumeration [Windows Media Player]","wmp.wmpburnstate","wmp/WMPBurnState","wmp/wmpbsBurning","wmp/wmpbsBusy","wmp/wmpbsErasing","wmp/wmpbsPreparingToBurn","wmp/wmpbsReady","wmp/wmpbsRefreshStatusPending","wmp/wmpbsStopped","wmp/wmpbsUnknown","wmp/wmpbsWaitingForDisc","wmpbsBurning","wmpbsBusy","wmpbsErasing","wmpbsPreparingToBurn","wmpbsReady","wmpbsRefreshStatusPending","wmpbsStopped","wmpbsUnknown","wmpbsWaitingForDisc"]
old-location: wmp\wmpburnstate.htm
tech.root: WMP
ms.assetid: fd286f68-4d36-48ae-800e-ad2be4c613c1
ms.date: 12/05/2018
ms.keywords: WMPBurnState, WMPBurnState enumeration [Windows Media Player], wmp.wmpburnstate, wmp/WMPBurnState, wmp/wmpbsBurning, wmp/wmpbsBusy, wmp/wmpbsErasing, wmp/wmpbsPreparingToBurn, wmp/wmpbsReady, wmp/wmpbsRefreshStatusPending, wmp/wmpbsStopped, wmp/wmpbsUnknown, wmp/wmpbsWaitingForDisc, wmpbsBurning, wmpbsBusy, wmpbsErasing, wmpbsPreparingToBurn, wmpbsReady, wmpbsRefreshStatusPending, wmpbsStopped, wmpbsUnknown, wmpbsWaitingForDisc
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
req.typenames: WMPBurnState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMPBurnState
 - wmp/WMPBurnState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmp.h
api_name:
 - WMPBurnState
---

# WMPBurnState enumeration


## -description

The <b>WMPBurnState</b> enumeration type defines the possible operational states of Windows Media Player as it burns a CD.

## -enum-fields

### -field wmpbsUnknown:0

Not a valid state.

### -field wmpbsBusy

Windows Media Player is busy. Try again in a moment.

### -field wmpbsReady

Ready to begin burning a CD.

### -field wmpbsWaitingForDisc

Waiting for the disc to become available.

### -field wmpbsRefreshStatusPending

The burn playlist has changed. Call <a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-refreshstatus">IWMPCdromBurn::refreshStatus</a>.

### -field wmpbsPreparingToBurn

Windows Media Player is preparing to burn the CD.

### -field wmpbsBurning

The CD is being burned.

### -field wmpbsStopped

The burning operation is stopped.

### -field wmpbsErasing

Windows Media Player is erasing the CD.

### -field wmpbsDownloading

## -remarks

Windows Media Player 10 Mobile: This enumeration is not supported.

## -see-also

<a href="/windows/desktop/WMP/enumeration-types">Enumeration Types</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>
