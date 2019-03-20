---
UID: NF:faxcom.IFaxPort.get_DeviceId
title: IFaxPort::get_DeviceId (faxcom.h)
author: windows-sdk-content
description: The IFaxPort::get_DeviceId property is a number representing the permanent line identifier for the fax port.
old-location: fax\_mfax_ifaxport_mfax_ifaxport_get_deviceid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8gf8.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeviceId property [Fax Service], DeviceId property [Fax Service],IFaxPort interface, IFaxPort interface [Fax Service],DeviceId property, IFaxPort.DeviceId, IFaxPort.get_DeviceId, IFaxPort::DeviceId, IFaxPort::get_DeviceId, _mfax_ifaxport_get_deviceid, fax._mfax_ifaxport_get_deviceid, fax._mfax_ifaxport_mfax_ifaxport_get_deviceid_cpp, faxcom/IFaxPort::DeviceId, faxcom/IFaxPort::get_DeviceId, get_DeviceId
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
 - IFaxPort.DeviceId
 - IFaxPort.get_DeviceId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxPort::get_DeviceId


## -description


The <b>IFaxPort::get_DeviceId</b> property is a number representing the permanent line identifier for the fax port. 

This property is read-only.


## -parameters


## -remarks



A fax client application can use the <b>IFaxPort::get_DeviceId</b> property to uniquely identify a fax port. A fax client can call the <a href="https://msdn.microsoft.com/en-us/library/ms690887(v=VS.85).aspx">IFaxPort::get_Name</a> property to retrieve the user-friendly name for the fax port. Note, however, that it is possible for multiple fax ports to have the same user-friendly name.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690887(v=VS.85).aspx">IFaxPort::get_Name</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>
 

 

