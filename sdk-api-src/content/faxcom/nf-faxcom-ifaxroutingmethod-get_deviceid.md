---
UID: NF:faxcom.IFaxRoutingMethod.get_DeviceId
title: IFaxRoutingMethod::get_DeviceId
author: windows-sdk-content
description: The DeviceId property is a number representing the line identifier for the fax port.
old-location: fax\_mfax_ifaxroutingmethod_get_deviceid_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_44h0.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: DeviceId property [Fax Service], DeviceId property [Fax Service],FaxRoutingMethod object, FaxRoutingMethod object [Fax Service],DeviceId property, FaxRoutingMethod.DeviceId, IFaxRoutingMethod.get_DeviceId, IFaxRoutingMethod::get_DeviceId, _mfax_ifaxroutingmethod_get_deviceid, fax._mfax_ifaxroutingmethod_get_deviceid, fax._mfax_ifaxroutingmethod_get_deviceid_vb, get_DeviceId
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - FaxRoutingMethod.DeviceId
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRoutingMethod::get_DeviceId


## -description


The <b>DeviceId</b> property is a number representing the line identifier for the fax port. 

This property is read-only.


## -parameters


## -remarks



A fax client application can use the <b>DeviceId</b> property to uniquely identify a fax port. You can call the <a href="https://msdn.microsoft.com/library/windows/hardware/mt188594">DeviceName</a> property to retrieve the user-friendly name for a port. Note, however, that it is possible for multiple fax ports to have the same user-friendly name.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt188594">DeviceName</a>



<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690703(v=VS.85).aspx">FaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>
 

 

