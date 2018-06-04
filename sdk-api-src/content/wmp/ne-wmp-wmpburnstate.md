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

# WMPBurnState enumeration


## -description



The <b>WMPBurnState</b> enumeration type defines the possible operational states of Windows Media Player as it burns a CD.




## -enum-fields




### -field wmpbsUnknown

Not a valid state.


### -field wmpbsBusy

Windows Media Player is busy. Try again in a moment.


### -field wmpbsReady

Ready to begin burning a CD.


### -field wmpbsWaitingForDisc

Waiting for the disc to become available.


### -field wmpbsRefreshStatusPending

The burn playlist has changed. Call <a href="https://msdn.microsoft.com/7a1ca071-0a61-4ef5-b8c1-18336cf5b1b0">IWMPCdromBurn::refreshStatus</a>.


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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/45116a33-62f9-4c7d-b246-25905cbaf118">IWMPCdromBurn Interface</a>
 

 

