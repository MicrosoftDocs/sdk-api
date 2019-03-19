---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetSupportedCommands
title: IPortableDeviceServiceCapabilities::GetSupportedCommands (portabledeviceapi.h)
author: windows-sdk-content
description: Retrieves the commands supported by the service.
old-location: wpdsdk\iportabledeviceservicecapabilities_getsupportedcommands.htm
tech.root: wpd_sdk
ms.assetid: b116ae11-f02f-47aa-8c54-4810e2d50046
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSupportedCommands, GetSupportedCommands method [Windows Portable Devices SDK], GetSupportedCommands method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],GetSupportedCommands method, IPortableDeviceServiceCapabilities.GetSupportedCommands, IPortableDeviceServiceCapabilities::GetSupportedCommands, portabledeviceapi/IPortableDeviceServiceCapabilities::GetSupportedCommands, wpdsdk.iportabledeviceservicecapabilities_getsupportedcommands
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceServiceCapabilities.GetSupportedCommands
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceServiceCapabilities::GetSupportedCommands


## -description


The <b>GetSupportedCommands</b> method retrieves the commands supported by the service.


## -parameters




### -param ppCommands [out]

The <a href="https://msdn.microsoft.com/2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd">IPortableDeviceKeyCollection</a> interface that receives the list of commands.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>
 

 

