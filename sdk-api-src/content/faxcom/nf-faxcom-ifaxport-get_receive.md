---
UID: NF:faxcom.IFaxPort.get_Receive
title: IFaxPort::get_Receive
author: windows-sdk-content
description: The IFaxPort::get_Receive property is a Boolean value that indicates whether a specified fax port is enabled to receive faxes.
old-location: fax\_mfax_ifaxport_mfax_ifaxport_get_receive_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8b1h.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxPort interface [Fax Service],Receive property, IFaxPort.Receive, IFaxPort.get_Receive, IFaxPort::Receive, IFaxPort::get_Receive, IFaxPort::put_Receive, Receive property [Fax Service], Receive property [Fax Service],IFaxPort interface, _mfax_ifaxport_get_receive, fax._mfax_ifaxport_get_receive, fax._mfax_ifaxport_mfax_ifaxport_get_receive_cpp, faxcom/IFaxPort::Receive, faxcom/IFaxPort::get_Receive, faxcom/IFaxPort::put_Receive, get_Receive
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
 - IFaxPort.Receive
 - IFaxPort.get_Receive
 - IFaxPort.put_Receive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxPort::get_Receive


## -description


The <b>IFaxPort::get_Receive</b> property is a Boolean value that indicates whether a specified fax port is enabled to receive faxes.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  Before setting a value for this property, a fax client application can call the <a href="https://msdn.microsoft.com/en-us/library/ms692798(v=VS.85).aspx">IFaxPort::get_CanModify</a> property to ensure that the client has permission to modify configuration information for the specified fax port.</div>
<div> </div>
The <b>IFaxPort::get_Receive</b> property returns a value of <b>TRUE</b> if the fax port is enabled to receive faxes. If a fax client application passes a value of <b>TRUE</b> to the property, it enables the fax port to receive faxes.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>
 

 

