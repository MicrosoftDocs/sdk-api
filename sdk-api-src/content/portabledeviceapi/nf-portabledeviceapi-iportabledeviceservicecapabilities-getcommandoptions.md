---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.GetCommandOptions
title: IPortableDeviceServiceCapabilities::GetCommandOptions method
author: windows-driver-content
description: Retrieves the options of a WPD command.
old-location: wpdsdk\iportabledeviceservicecapabilities_getcommandoptions.htm
old-project: wpd_sdk
ms.assetid: 5baa4c94-771a-430f-a963-800e4cd3a6b3
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: GetCommandOptions method [Windows Portable Devices SDK], GetCommandOptions method [Windows Portable Devices SDK], IPortableDeviceServiceCapabilities interface, GetCommandOptions,IPortableDeviceServiceCapabilities.GetCommandOptions, IPortableDeviceServiceCapabilities, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK], GetCommandOptions method, IPortableDeviceServiceCapabilities::GetCommandOptions, portabledeviceapi/IPortableDeviceServiceCapabilities::GetCommandOptions, wpdsdk.iportabledeviceservicecapabilities_getcommandoptions
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
-	IPortableDeviceServiceCapabilities.GetCommandOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPortableDeviceServiceCapabilities::GetCommandOptions method


## -description


The <b>GetCommandOptions</b> method retrieves the options of a WPD command.


## -parameters




### -param Command [in]

The command whose options are retrieved.


### -param ppOptions [out]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that receives the list of options.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>
 

 

