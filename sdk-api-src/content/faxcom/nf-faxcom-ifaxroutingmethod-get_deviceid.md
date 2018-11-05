---
UID: NF:faxcom.IFaxRoutingMethod.get_DeviceId
title: IFaxRoutingMethod::get_DeviceId
author: windows-sdk-content
description: The IFaxRoutingMethod::get_DeviceId property is a number representing the line identifier for the fax port.
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_deviceid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_44h0.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DeviceId property [Fax Service], DeviceId property [Fax Service],IFaxRoutingMethod interface, IFaxRoutingMethod interface [Fax Service],DeviceId property, IFaxRoutingMethod.DeviceId, IFaxRoutingMethod.get_DeviceId, IFaxRoutingMethod::DeviceId, IFaxRoutingMethod::get_DeviceId, _mfax_ifaxroutingmethod_get_deviceid, fax._mfax_ifaxroutingmethod_get_deviceid, fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_deviceid_cpp, faxcom/IFaxRoutingMethod::DeviceId, faxcom/IFaxRoutingMethod::get_DeviceId, get_DeviceId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxRoutingMethod.DeviceId
 - IFaxRoutingMethod.get_DeviceId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxRoutingMethod::get_DeviceId


## -description


The <b>IFaxRoutingMethod::get_DeviceId</b> property is a number representing the line identifier for the fax port. 

This property is read-only.


## -parameters


## -remarks



A fax client application can use the <b>IFaxRoutingMethod::get_DeviceId</b> property to uniquely identify a fax port. You can call the <a href="https://msdn.microsoft.com/ae0cc37c-bfc8-4e89-a3a4-b06a3917f835">IFaxRoutingMethod::get_DeviceName</a> property to retrieve the user-friendly name for a port. Note, however, that it is possible for multiple fax ports to have the same user-friendly name.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>



<a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/ae0cc37c-bfc8-4e89-a3a4-b06a3917f835">IFaxRoutingMethod::get_DeviceName</a>



<a href="https://msdn.microsoft.com/8dfab525-4eda-42b9-ac02-c8c25575d0aa">IFaxRoutingMethods</a>
 

 

