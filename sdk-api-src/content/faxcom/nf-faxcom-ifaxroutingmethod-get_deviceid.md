---
UID: NF:faxcom.IFaxRoutingMethod.get_DeviceId
title: IFaxRoutingMethod::get_DeviceId method
author: windows-driver-content
description: The DeviceId property is a number representing the line identifier for the fax port.
old-location: fax\_mfax_ifaxroutingmethod_get_deviceid_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_44h0.htm
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: DeviceId property [Fax Service], DeviceId property [Fax Service], FaxRoutingMethod object, FaxRoutingMethod object [Fax Service], DeviceId property, IFaxRoutingMethod, IFaxRoutingMethod::get_DeviceId, _mfax_ifaxroutingmethod_get_deviceid, fax._mfax_ifaxroutingmethod_get_deviceid, fax._mfax_ifaxroutingmethod_get_deviceid_vb, get_DeviceId,IFaxRoutingMethod.get_DeviceId
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
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Faxcom.dll
api_name:
-	FaxRoutingMethod.DeviceId
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRoutingMethod::get_DeviceId method


## -description


The <b>DeviceId</b> property is a number representing the line identifier for the fax port. 

This property is read-only.


## -parameters


## -remarks



A fax client application can use the <b>DeviceId</b> property to uniquely identify a fax port. You can call the <a href="https://msdn.microsoft.com/library/windows/hardware/mt188594">DeviceName</a> property to retrieve the user-friendly name for a port. Note, however, that it is possible for multiple fax ports to have the same user-friendly name.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt188594">DeviceName</a>



<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/4ae5aa09-2961-4823-8c39-0b0a5b0bdc81">FaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>



<a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/8dfab525-4eda-42b9-ac02-c8c25575d0aa">IFaxRoutingMethods</a>
 

 

