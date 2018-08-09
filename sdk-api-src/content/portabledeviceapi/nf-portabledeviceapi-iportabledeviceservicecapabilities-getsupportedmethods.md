---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetSupportedMethods
title: IPortableDeviceServiceCapabilities::GetSupportedMethods
author: windows-sdk-content
description: Retrieves the methods supported by the service.
old-location: wpdsdk\iportabledeviceservicecapabilities_getsupportedmethods.htm
old-project: wpd_sdk
ms.assetid: 60201d12-5a49-4d84-9dae-b04cbb144d8f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetSupportedMethods, GetSupportedMethods method [Windows Portable Devices SDK], GetSupportedMethods method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetSupportedMethods method, IPortableDeviceServiceCapabilities.GetSupportedMethods, IPortableDeviceServiceCapabilities::GetSupportedMethods, portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedMethods, wpdsdk.iportabledeviceservicecapabilities_getsupportedmethods
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceServiceCapabilities.GetSupportedMethods
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceServiceCapabilities::GetSupportedMethods


## -description


The <b>GetSupportedMethods</b> method retrieves the methods supported by the service.


## -parameters




### -param ppMethods [out]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597589">IPortableDevicePropVariantCollection</a> interface that receives the list of methods.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>



<a href="https://msdn.microsoft.com/783a6552-9b22-4af4-9252-b443e2624687">Retrieving Supported Service Methods</a>
 

 

