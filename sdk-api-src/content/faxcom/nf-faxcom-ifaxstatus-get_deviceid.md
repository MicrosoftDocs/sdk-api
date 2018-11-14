---
UID: NF:faxcom.IFaxStatus.get_DeviceId
title: IFaxStatus::get_DeviceId
author: windows-sdk-content
description: Retrieves the DeviceId property for the FaxStatus object of a parent FaxPort object. The DeviceId property is a number representing the permanent line identifier for the fax port.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_deviceid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_097o.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: DeviceId property [Fax Service], DeviceId property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],DeviceId property, IFaxStatus.DeviceId, IFaxStatus.get_DeviceId, IFaxStatus::DeviceId, IFaxStatus::get_DeviceId, _mfax_ifaxstatus_get_deviceid, fax._mfax_ifaxstatus_get_deviceid, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_deviceid_cpp, faxcom/IFaxStatus::DeviceId, faxcom/IFaxStatus::get_DeviceId, get_DeviceId
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
 - IFaxStatus.DeviceId
 - IFaxStatus.get_DeviceId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcom.h
: 
- IFaxStatus.get_DeviceId
: 
---

# IFaxStatus::get_DeviceId


## -description


Retrieves the <b>DeviceId</b> property for the <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>DeviceId</b> property is a number representing the permanent line identifier for the fax port.

This property is read-only.


## -parameters


## -remarks



It is possible for multiple fax ports to have the same user-friendly name. You can use the <b>DeviceId</b> property to uniquely identify a fax port, and thereby associate a <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object with a <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a>
 

 

