---
UID: NE:wmp.WMPSyncState
title: WMPSyncState
author: windows-sdk-content
description: The WMPSyncState enumeration type defines the possible operational states of Windows Media Player as it synchronizes digital media to a device. To use this enumeration you must create a remoted instance of the Windows Media Player 10 or later control.
old-location: wmp\wmpsyncstate.htm
old-project: WMP
ms.assetid: 8f1e8026-bbde-42bc-8ac8-555cc363b0b9
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: WMPSyncState, WMPSyncState enumeration [Windows Media Player], wmp.wmpsyncstate, wmp/WMPSyncState, wmp/wmpssEstimating, wmp/wmpssLast, wmp/wmpssStopped, wmp/wmpssSynchronizing, wmp/wmpssUnknown, wmpssEstimating, wmpssLast, wmpssStopped, wmpssSynchronizing, wmpssUnknown
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wmp.h
api_name:
-	WMPSyncState
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/98970d33-8035-49f9-9243-b4832df6e5c9">IWMPEvents2::DeviceSyncStateChange</a>



<a href="https://msdn.microsoft.com/49b07233-df9d-4fd0-836e-62b992408018">IWMPSyncDevice3::estimateSyncSize</a>



<a href="https://msdn.microsoft.com/c93263a1-7976-43db-b514-97d9a263a60c">IWMPSyncDevice::get_syncState</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

