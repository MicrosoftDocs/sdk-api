---
UID: NE:wmp.WMPSyncState
title: WMPSyncState
author: windows-sdk-content
description: The WMPSyncState enumeration type defines the possible operational states of Windows Media Player as it synchronizes digital media to a device. To use this enumeration you must create a remoted instance of the Windows Media Player 10 or later control.
old-location: wmp\wmpsyncstate.htm
tech.root: WMP
ms.assetid: 8f1e8026-bbde-42bc-8ac8-555cc363b0b9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WMPSyncState, WMPSyncState enumeration [Windows Media Player], wmp.wmpsyncstate, wmp/WMPSyncState, wmp/wmpssEstimating, wmp/wmpssLast, wmp/wmpssStopped, wmp/wmpssSynchronizing, wmp/wmpssUnknown, wmpssEstimating, wmpssLast, wmpssStopped, wmpssSynchronizing, wmpssUnknown
ms.topic: enum
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




<a href="https://msdn.microsoft.com/90689fb7-656d-4c06-a0a9-02bbe0e5b5dd">Enumeration Types</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563295(v=VS.85).aspx">IWMPEvents2::DeviceSyncStateChange</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563715(v=VS.85).aspx">IWMPSyncDevice3::estimateSyncSize</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563742(v=VS.85).aspx">IWMPSyncDevice::get_syncState</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

