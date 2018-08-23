---
UID: NF:upnp.IUPnPDevice.get_ModelURL
title: IUPnPDevice::get_ModelURL
author: windows-sdk-content
description: The ModelURL property specifies the URL for a Web page that contains model-specific information for the device.
old-location: upnp\iupnpdevice_modelurl.htm
old-project: upnp
ms.assetid: e9f3231a-5836-4629-9df5-6ed9184fb753
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_ModelURL method, IUPnPDevice.get_ModelURL, IUPnPDevice::get_ModelURL, _upnp_iupnpdevice_modelurl, get_ModelURL, get_ModelURL method [UPnP APIs], get_ModelURL method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_modelurl, upnp/IUPnPDevice::get_ModelURL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDevice.get_ModelURL
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDevice::get_ModelURL


## -description


The 
<b>ModelURL</b> property specifies the URL for a Web page that contains model-specific information for the device.


## -parameters




### -param pbstr [out]

Receives a reference to a string that contains the URL. Release this string with <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when it is no longer required. If the device does not specify this URL, this parameter is set to <b>NULL</b>.


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. If the device does not specify this URL, the return value is S_FALSE and <i>pbstr</i> is <b>NULL</b>. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



This property is optional and <i>pbstr</i> can be <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>



<a href="https://msdn.microsoft.com/c71868ab-e05d-4e6a-b157-4474afc8f61f">IUPnPDevice::ModelName</a>



<a href="https://msdn.microsoft.com/7e9b92a6-efad-41f0-b083-a2fed0f70c8b">IUPnPDevice::ModelNumber</a>
 

 

