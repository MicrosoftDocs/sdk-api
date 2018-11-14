---
UID: NF:wmp.IWMPEvents2.DeviceSyncStateChange
title: IWMPEvents2::DeviceSyncStateChange
author: windows-sdk-content
description: The DeviceSyncStateChange event occurs when the synchronization state of a device changes.
old-location: wmp\iwmpevents2_iwmpevents2__devicesyncstatechange.htm
tech.root: WMP
ms.assetid: 98970d33-8035-49f9-9243-b4832df6e5c9
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: DeviceSyncStateChange, DeviceSyncStateChange method [Windows Media Player], DeviceSyncStateChange method [Windows Media Player],IWMPEvents2 interface, IWMPEvents2 interface [Windows Media Player],DeviceSyncStateChange method, IWMPEvents2.DeviceSyncStateChange, IWMPEvents2::DeviceSyncStateChange, IWMPEvents2DeviceSyncStateChange, wmp.iwmpevents2_iwmpevents2__devicesyncstatechange, wmp/IWMPEvents2::DeviceSyncStateChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents2.DeviceSyncStateChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmp.h
: 
- IWMPEvents2.DeviceSyncStateChange
: 
---

# IWMPEvents2::DeviceSyncStateChange


## -description



The <b>DeviceSyncStateChange</b> event occurs when the synchronization state of a device changes.




## -parameters




### -param pDevice [in]

Address of the <b>IWMPSyncDevice</b> interface that represents the device for which the synchronization state changed.


### -param NewState [in]

<b>WMPSyncState</b> enumeration value that represents the new synchronization state for the device specified by <i>pDevice</i>.


## -returns



This method does not return a value.




## -remarks



Use <b>IWMPSyncDevice::isIdentical</b> to determine whether a particular device matches the device for which the synchronization state changed.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/61cd0a2e-b94f-4c10-b3e2-ad1dc2a0b17d">IWMPEvents2 Interface</a>



<a href="https://msdn.microsoft.com/4335d480-5af0-4764-b8f8-0e6edc1598b7">IWMPSyncDevice::isIdentical</a>



<a href="https://msdn.microsoft.com/8f1e8026-bbde-42bc-8ac8-555cc363b0b9">WMPSyncState</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 

