---
UID: NF:wmp.IWMPEvents2.DeviceStatusChange
title: IWMPEvents2::DeviceStatusChange
author: windows-sdk-content
description: The DeviceStatusChange event occurs when the partnership status of a device changes.
old-location: wmp\iwmpevents2_iwmpevents2__devicestatuschange.htm
tech.root: WMP
ms.assetid: f9781dde-e813-4e2d-820d-5a0803bfbe4e
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DeviceStatusChange, DeviceStatusChange method [Windows Media Player], DeviceStatusChange method [Windows Media Player],IWMPEvents2 interface, IWMPEvents2 interface [Windows Media Player],DeviceStatusChange method, IWMPEvents2.DeviceStatusChange, IWMPEvents2::DeviceStatusChange, IWMPEvents2DeviceStatusChange, wmp.iwmpevents2_iwmpevents2__devicestatuschange, wmp/IWMPEvents2::DeviceStatusChange
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
 - IWMPEvents2.DeviceStatusChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents2::DeviceStatusChange


## -description



The <b>DeviceStatusChange</b> event occurs when the partnership status of a device changes.




## -parameters




### -param pDevice [in]

Address of the <b>IWMPSyncDevice</b> interface that represents the device for which the status changed.


### -param NewStatus [in]

<b>WMPDeviceStatus</b> enumeration value that represents the new status for the device specified by <i>pDevice</i>.


## -returns



This method does not return a value.




## -remarks



Use <b>IWMPSyncDevice::isIdentical</b> to determine whether a particular device matches the device for which the status changed.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/61cd0a2e-b94f-4c10-b3e2-ad1dc2a0b17d">IWMPEvents2 Interface</a>



<a href="https://msdn.microsoft.com/4335d480-5af0-4764-b8f8-0e6edc1598b7">IWMPSyncDevice::isIdentical</a>



<a href="https://msdn.microsoft.com/dbbb97f8-4b26-4add-a661-a48eff8ad0f5">WMPDeviceStatus</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 

