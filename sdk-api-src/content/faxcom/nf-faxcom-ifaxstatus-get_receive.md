---
UID: NF:faxcom.IFaxStatus.get_Receive
title: IFaxStatus::get_Receive
author: windows-sdk-content
description: Retrieves the Receive property for the FaxStatus object of a parent FaxPort object. The Receive property is a Boolean value that indicates whether a specified fax port is currently receiving a fax.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_receive_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5u1x.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IFaxStatus interface [Fax Service],Receive property, IFaxStatus.Receive, IFaxStatus.get_Receive, IFaxStatus::Receive, IFaxStatus::get_Receive, Receive property [Fax Service], Receive property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_receive, fax._mfax_ifaxstatus_get_receive, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_receive_cpp, faxcom/IFaxStatus::Receive, faxcom/IFaxStatus::get_Receive, get_Receive
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
 - IFaxStatus.Receive
 - IFaxStatus.get_Receive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxStatus::get_Receive


## -description


Retrieves the <b>Receive</b> property for the <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>Receive</b> property is a Boolean value that indicates whether a specified fax port is currently receiving a fax.

This property is read-only.


## -parameters


## -remarks



To determine if a specified port is currently sending a fax, you can call the <a href="https://msdn.microsoft.com/239b98c5-be46-4e54-83f7-eb7f6250fa57">IFaxStatus::get_Send</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/239b98c5-be46-4e54-83f7-eb7f6250fa57">IFaxStatus::get_Send</a>
 

 

