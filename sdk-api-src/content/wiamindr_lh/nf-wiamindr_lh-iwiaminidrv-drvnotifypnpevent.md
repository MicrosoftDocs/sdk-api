---
UID: NF:wiamindr_lh.IWiaMiniDrv.drvNotifyPnpEvent
title: IWiaMiniDrv::drvNotifyPnpEvent method
author: windows-driver-content
description: The IWiaMiniDrv::drvNotifyPnpEvent method responds to the event received from the WIA service.
old-location: image\iwiaminidrv_drvnotifypnpevent.htm
old-project: image
ms.assetid: 55d6d93b-c20f-435b-ba99-2df26bd17240
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaMiniDrv, IWiaMiniDrv interface [Imaging Devices], drvNotifyPnpEvent method, IWiaMiniDrv::drvNotifyPnpEvent, MiniDrv_7684a7e5-7ca5-4d20-a1a8-fc38400815ce.xml, drvNotifyPnpEvent method [Imaging Devices], drvNotifyPnpEvent method [Imaging Devices], IWiaMiniDrv interface, drvNotifyPnpEvent,IWiaMiniDrv.drvNotifyPnpEvent, image.iwiaminidrv_drvnotifypnpevent, wiamindr_lh/IWiaMiniDrv::drvNotifyPnpEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wiamindr_lh.h
req.include-header: Wiamindr.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Me and in Windows XP and later.
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
req.typenames: SCANWINDOW, *PSCANWINDOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wiamindr_lh.h
api_name:
-	IWiaMiniDrv.drvNotifyPnpEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaMiniDrv::drvNotifyPnpEvent method


## -description


The <b>IWiaMiniDrv::drvNotifyPnpEvent</b> method responds to the event received from the WIA service.


## -parameters




### -param pEventGUID




### -param bstrDeviceID [in]

Specifies a string containing the device's unique identifier. 


### -param ulReserved [in]

Is reserved for system use.


#### - pEventGuid [in]

Points to a GUID identifying the event.


## -returns



On success, the method should return S_OK. If the method fails, it should return a standard COM error code.




## -remarks



The WIA service notifies a WIA minidriver of a supported device event by calling the <b>IWiaMiniDrv::drvNotifyPnpEvent</b> method. In this method the minidriver implements the device-specific functionality needed to respond to the event.

If this method is called with *<i>pEventGuid</i> set to WIA_EVENT_CANCEL_IO device event (described in the Microsoft Windows SDK documentation), it should cancel all current I/O operations as soon as possible.




## -see-also




<a href="https://msdn.microsoft.com/15068d10-5e24-427c-9684-24ce67b75ada">IWiaMiniDrv</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543977">IWiaMiniDrv::drvGetCapabilities</a>
 

 

