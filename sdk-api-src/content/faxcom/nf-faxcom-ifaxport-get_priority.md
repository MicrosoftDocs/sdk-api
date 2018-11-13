---
UID: NF:faxcom.IFaxPort.get_Priority
title: IFaxPort::get_Priority
author: windows-sdk-content
description: The IFaxPort::get_Priority property is a number representing the transmission priority designated for a specified fax port. Priority determines the relative order in which available fax devices send outgoing transmissions.
old-location: fax\_mfax_ifaxport_mfax_ifaxport_get_priority_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0515.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxPort interface [Fax Service],Priority property, IFaxPort.Priority, IFaxPort.get_Priority, IFaxPort::Priority, IFaxPort::get_Priority, IFaxPort::put_Priority, Priority property [Fax Service], Priority property [Fax Service],IFaxPort interface, _mfax_ifaxport_get_priority, fax._mfax_ifaxport_get_priority, fax._mfax_ifaxport_mfax_ifaxport_get_priority_cpp, faxcom/IFaxPort::Priority, faxcom/IFaxPort::get_Priority, faxcom/IFaxPort::put_Priority, get_Priority
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
 - IFaxPort.Priority
 - IFaxPort.get_Priority
 - IFaxPort.put_Priority
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxPort::get_Priority


## -description


The <b>IFaxPort::get_Priority</b> property is a number representing the transmission priority designated for a specified fax port. Priority determines the relative order in which available fax devices send outgoing transmissions.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  Before setting a value for this property, a fax client application can call the <a href="https://msdn.microsoft.com/b09b6e5f-fa1d-4d0b-8581-e0ba779b72bb">IFaxPort::get_CanModify</a> property to ensure that the client has permission to modify configuration information for the specified fax port.</div>
<div> </div>
When the fax server initiates an outgoing fax transmission, it chooses the fax port with the highest priority and send capability. If that port is not available, the server selects the next available port that follows in rank order, and so on. When a client application changes the priority for a fax port, the fax service adjusts the priority for the other fax ports attached to the server. The <b>IFaxPort::get_Priority</b> property has no effect on incoming transmissions.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>
 

 

