---
UID: NF:faxcom.IFaxPort.get_DeviceId
title: IFaxPort::get_DeviceId
author: windows-sdk-content
description: The DeviceId property is a number representing the permanent line identifier for the fax port.
old-location: fax\_mfax_ifaxport_get_deviceid_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8gf8.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: DeviceId property [Fax Service], DeviceId property [Fax Service],FaxPort object, FaxPort object [Fax Service],DeviceId property, FaxPort.DeviceId, IFaxPort.get_DeviceId, IFaxPort::get_DeviceId, _mfax_ifaxport_get_deviceid, fax._mfax_ifaxport_get_deviceid, fax._mfax_ifaxport_get_deviceid_vb, get_DeviceId
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Faxcom.dll
api_name:
-	FaxPort.DeviceId
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxPort::get_DeviceId


## -description


The <b>DeviceId</b> property is a number representing the permanent line identifier for the fax port. 

This property is read-only.


## -parameters


## -remarks



A fax client application can use the <b>DeviceId</b> property to uniquely identify a fax port. A fax client can call the <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> property to retrieve the user-friendly name for the fax port. Note, however, that it is possible for multiple fax ports to have the same user-friendly name.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/7888d042-7d85-4921-b233-f6e95e0c80d9">FaxPort</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>
 

 

