---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetSupportedMethodsByFormat
title: IPortableDeviceServiceCapabilities::GetSupportedMethodsByFormat method
author: windows-driver-content
description: Retrieves the methods supported by the service for the specified format.
old-location: wpdsdk\iportabledeviceservicecapabilities_getsupportedmethodsbyformat.htm
old-project: wpd_sdk
ms.assetid: f1950aa5-2316-4409-a7bd-1b87c6449187
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: GetSupportedMethodsByFormat method [Windows Portable Devices SDK], GetSupportedMethodsByFormat method [Windows Portable Devices SDK], IPortableDeviceServiceCapabilities interface, GetSupportedMethodsByFormat,IPortableDeviceServiceCapabilities.GetSupportedMethodsByFormat, IPortableDeviceServiceCapabilities, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK], GetSupportedMethodsByFormat method, IPortableDeviceServiceCapabilities::GetSupportedMethodsByFormat, portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedMethodsByFormat, wpdsdk.iportabledeviceservicecapabilities_getsupportedmethodsbyformat
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
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceAPI.h
api_name:
-	IPortableDeviceServiceCapabilities.GetSupportedMethodsByFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPortableDeviceServiceCapabilities::GetSupportedMethodsByFormat method


## -description


The <b>GetSupportedMethodsByFormat</b> method  retrieves the methods supported by the service for the specified format.


## -parameters




### -param Format [in]

The format whose supported methods are retrieved.


### -param ppMethods [out]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597589">IPortableDevicePropVariantCollection</a> interface that receives the list of methods.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>
 

 

