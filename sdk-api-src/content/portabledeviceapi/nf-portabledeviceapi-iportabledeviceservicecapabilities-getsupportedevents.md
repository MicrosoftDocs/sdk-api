---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetSupportedEvents
title: IPortableDeviceServiceCapabilities::GetSupportedEvents method
author: windows-driver-content
description: Retrieves the events supported by the service.
old-location: wpdsdk\iportabledeviceservicecapabilities_getsupportedevents.htm
old-project: wpd_sdk
ms.assetid: 19621abc-34df-4c16-8cb7-f0d9d7fb7e06
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetSupportedEvents method [Windows Portable Devices SDK], GetSupportedEvents method [Windows Portable Devices SDK], IPortableDeviceServiceCapabilities interface, GetSupportedEvents,IPortableDeviceServiceCapabilities.GetSupportedEvents, IPortableDeviceServiceCapabilities, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK], GetSupportedEvents method, IPortableDeviceServiceCapabilities::GetSupportedEvents, portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedEvents, wpdsdk.iportabledeviceservicecapabilities_getsupportedevents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: PortableDeviceAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WPD_WHITE_BALANCE_SETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceAPI.h
api_name:
-	IPortableDeviceServiceCapabilities.GetSupportedEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceServiceCapabilities::GetSupportedEvents method


## -description


The <b>GetSupportedEvents</b> method retrieves the events supported by the service.


## -parameters




### -param ppEvents [out]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597589">IPortableDevicePropVariantCollection</a> interface that receives the list of events.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>
 

 

