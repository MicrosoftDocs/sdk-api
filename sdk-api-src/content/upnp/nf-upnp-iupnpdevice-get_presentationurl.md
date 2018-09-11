---
UID: NF:upnp.IUPnPDevice.get_PresentationURL
title: IUPnPDevice::get_PresentationURL
author: windows-sdk-content
description: The PresentationURL property specifies the presentation URL for a Web page that controls the device.
old-location: upnp\iupnpdevice_presentationurl.htm
tech.root: UPnP
ms.assetid: 8dba8289-2f2f-482c-abd6-38f81a11f5e2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_PresentationURL method, IUPnPDevice.get_PresentationURL, IUPnPDevice::get_PresentationURL, _upnp_iupnpdevice_presentationurl, get_PresentationURL, get_PresentationURL method [UPnP APIs], get_PresentationURL method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_presentationurl, upnp/IUPnPDevice::get_PresentationURL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: upnp.h
req.include-header: 
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
req.lib: 
req.dll: Upnp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDevice.get_PresentationURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPDevice::get_PresentationURL


## -description


The 
<b>PresentationURL</b> property specifies the presentation URL for a Web page that controls the device.


## -parameters




### -param pbstr [out]

Receives a reference to a string that contains the presentation URL for the Web page. This URL is an absolute URL. Release this string with <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> when it is no longer used. If the device does not specify a presentation URL, this parameter receives an empty string.


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. If the device did not specify a presentation URL, the return value is S_FALSE. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks




<div class="alert"><b>Note</b>  This property  must not be empty and must contain a valid URL.</div>
<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>
 

 

