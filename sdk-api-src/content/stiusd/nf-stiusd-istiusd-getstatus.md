---
UID: NF:stiusd.IStiUSD.GetStatus
title: IStiUSD::GetStatus method
author: windows-driver-content
description: A still image minidriver's IStiUSD::GetStatus method returns the status of a still image device.
old-location: image\istiusd_getstatus.htm
old-project: image
ms.assetid: 24133d1d-eac4-4740-9635-1205f7a2c4d4
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetStatus method [Imaging Devices], GetStatus method [Imaging Devices], IStiUSD interface, GetStatus,IStiUSD.GetStatus, IStiUSD, IStiUSD interface [Imaging Devices], GetStatus method, IStiUSD::GetStatus, image.istiusd_getstatus, stifnc_78892dba-6e94-4455-8616-f5c3afd9256e.xml, stiusd/IStiUSD::GetStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: stiusd.h
req.include-header: Stiusd.h
req.target-type: Desktop
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
req.typenames: SEC_WINNT_CREDUI_CONTEXT_VECTOR, *PSEC_WINNT_CREDUI_CONTEXT_VECTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	stiusd.h
api_name:
-	IStiUSD.GetStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IStiUSD::GetStatus method


## -description


A still image minidriver's <b>IStiUSD::GetStatus</b> method returns the status of a still image device.


## -parameters




### -param pDevStatus

Caller-supplied pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff548369">STI_DEVICE_STATUS</a> structure.


## -returns



If the operation succeeds, the method should return S_OK. Otherwise, it should return one of the STIERR-prefixed error codes defined in <i>stierr.h</i>.




## -remarks



The caller supplies values for the <b>dwSize</b> and <b>StatusMask</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548369">STI_DEVICE_STATUS</a> structure, and the minidriver must supply values for the rest of the structure members.

If the driver has previously set the STI_GENCAP_POLLING_NEEDED flag in the device's <a href="https://msdn.microsoft.com/library/windows/hardware/ff548380">STI_DEV_CAPS</a> structure, the minidriver's <b>IStiUSD::GetStatus</b> method is the means by which the event monitor determines if a <a href="https://msdn.microsoft.com/5f9be89c-8442-4894-b2f6-a4d3558464bf">Still Image Device Events</a> has occurred. The event monitor will call the method, specifying STI_DEVSTATUS_EVENT_STATE in the supplied <a href="https://msdn.microsoft.com/library/windows/hardware/ff548369">STI_DEVICE_STATUS</a> structure. The driver must poll the device and set STI_EVENTHANDLING_PENDING if an event has occurred.

If the caller specifies STI_DEVSTATUS_ONLINE_STATE in the supplied STI_DEVICE_STATUS structure, the minidriver should set the appropriate flag in the structure's <b>dwOnlineState</b> member.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543752">IStiDevice::GetStatus</a>



<a href="https://msdn.microsoft.com/62740263-5bbb-48e1-be3d-9ee9cb37d6b9">IStiUSD</a>
 

 

