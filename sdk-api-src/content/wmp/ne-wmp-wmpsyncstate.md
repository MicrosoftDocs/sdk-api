---
UID: NE:wmp.WMPSyncState
title: WMPSyncState (wmp.h)
author: windows-sdk-content
description: The WMPSyncState enumeration type defines the possible operational states of Windows Media Player as it synchronizes digital media to a device. To use this enumeration you must create a remoted instance of the Windows Media Player 10 or later control.
old-location: wmp\wmpsyncstate.htm
tech.root: WMP
ms.assetid: 8f1e8026-bbde-42bc-8ac8-555cc363b0b9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WMPSyncState, WMPSyncState enumeration [Windows Media Player], wmp.wmpsyncstate, wmp/WMPSyncState, wmp/wmpssEstimating, wmp/wmpssLast, wmp/wmpssStopped, wmp/wmpssSynchronizing, wmp/wmpssUnknown, wmpssEstimating, wmpssLast, wmpssStopped, wmpssSynchronizing, wmpssUnknown
ms.topic: enum
f1_keywords: 
 - "wmp/WMPSyncState"
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmp.h
api_name:
 - WMPSyncState
product: Windows
targetos: Windows
req.typenames: WMPSyncState
req.redist: 
ms.custom: 19H1
---

# WMPSyncState enumeration


## -description



The <b>WMPSyncState</b> enumeration type defines the possible operational states of Windows Media Player as it synchronizes digital media to a device. To use this enumeration you must create a remoted instance of the Windows Media Player 10 or later control.




## -enum-fields




### -field wmpssUnknown

Synchronization state is unknown.


### -field wmpssSynchronizing

Windows Media Player is synchronizing the device.


### -field wmpssStopped

Synchronization has stopped.


### -field wmpssEstimating

An estimation of synchronization size is in progress. Requires Windows Media Player 12.


### -field wmpssLast

Last enumerated value. Not a valid state.


## -remarks



Windows Media Player 10 Mobile: This enumeration is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/enumeration-types">Enumeration Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicesyncstatechange">IWMPEvents2::DeviceSyncStateChange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize">IWMPSyncDevice3::estimateSyncSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_syncstate">IWMPSyncDevice::get_syncState</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>
 

 

