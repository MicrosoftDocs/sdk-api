---
UID: NF:wmp.IWMPEvents2.DeviceDisconnect
title: IWMPEvents2::DeviceDisconnect (wmp.h)
author: windows-sdk-content
description: The DeviceDisconnect event occurs when the user disconnects a device from the computer.
old-location: wmp\iwmpevents2_iwmpevents2__devicedisconnect.htm
tech.root: WMP
ms.assetid: a37b72f9-4f71-433c-afad-66caae2d749a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeviceDisconnect, DeviceDisconnect method [Windows Media Player], DeviceDisconnect method [Windows Media Player],IWMPEvents2 interface, IWMPEvents2 interface [Windows Media Player],DeviceDisconnect method, IWMPEvents2.DeviceDisconnect, IWMPEvents2::DeviceDisconnect, IWMPEvents2DeviceDisconnect, wmp.iwmpevents2_iwmpevents2__devicedisconnect, wmp/IWMPEvents2::DeviceDisconnect
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
 - IWMPEvents2.DeviceDisconnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents2::DeviceDisconnect


## -description



The <b>DeviceDisconnect</b> event occurs when the user disconnects a device from the computer.




## -parameters




### -param pDevice [in]

Address of the <b>IWMPSyncDevice</b> interface that represents the device that the user disconnected.


## -returns



This method does not return a value.




## -remarks



Use <b>IWMPSyncDevice::isIdentical</b> to determine whether a particular device matches the device that the user disconnected.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563289(v=VS.85).aspx">IWMPEvents2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563743(v=VS.85).aspx">IWMPSyncDevice::isIdentical</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 

