---
UID: NF:wmp.IWMPEvents2.DeviceConnect
title: IWMPEvents2::DeviceConnect
author: windows-sdk-content
description: The DeviceConnect event occurs when the user connects a device to the computer.
old-location: wmp\iwmpevents2_iwmpevents2__deviceconnect.htm
old-project: WMP
ms.assetid: ed726579-e0cb-4007-98eb-b6df4b636b12
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: DeviceConnect, DeviceConnect method [Windows Media Player], DeviceConnect method [Windows Media Player],IWMPEvents2 interface, IWMPEvents2 interface [Windows Media Player],DeviceConnect method, IWMPEvents2.DeviceConnect, IWMPEvents2::DeviceConnect, IWMPEvents2DeviceConnect, wmp.iwmpevents2_iwmpevents2__deviceconnect, wmp/IWMPEvents2::DeviceConnect
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPEvents2.DeviceConnect
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents2::DeviceConnect


## -description



The <b>DeviceConnect</b> event occurs when the user connects a device to the computer.




## -parameters




### -param pDevice [in]

Address of the <b>IWMPSyncDevice</b> interface that represents the device that the user connected.


## -returns



This method does not return a value.




## -remarks



You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/61cd0a2e-b94f-4c10-b3e2-ad1dc2a0b17d">IWMPEvents2 Interface</a>



<a href="https://msdn.microsoft.com/4335d480-5af0-4764-b8f8-0e6edc1598b7">IWMPSyncDevice::isIdentical</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 

