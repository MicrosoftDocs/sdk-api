---
UID: NF:faxcom.IFaxRoutingMethod.get_DeviceId
title: IFaxRoutingMethod::get_DeviceId
author: windows-sdk-content
description: The IFaxRoutingMethod::get_DeviceId property is a number representing the line identifier for the fax port.
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_deviceid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_44h0.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
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




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/ae0cc37c-bfc8-4e89-a3a4-b06a3917f835">IFaxRoutingMethod::get_DeviceName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>
 

 

