---
UID: NF:faxcom.IFaxStatus.get_Receive
title: IFaxStatus::get_Receive
author: windows-sdk-content
description: Retrieves the Receive property for the FaxStatus object of a parent FaxPort object. The Receive property is a Boolean value that indicates whether a specified fax port is currently receiving a fax.
old-location: fax\_mfax_ifaxstatus_get_receive_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5u1x.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: FaxStatus object [Fax Service],Receive property, FaxStatus.Receive, IFaxStatus.get_Receive, IFaxStatus::get_Receive, Receive property [Fax Service], Receive property [Fax Service],FaxStatus object, _mfax_ifaxstatus_get_receive, fax._mfax_ifaxstatus_get_receive, fax._mfax_ifaxstatus_get_receive_vb, get_Receive
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
 - FaxStatus.Receive
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxStatus::get_Receive


## -description


Retrieves the <b>Receive</b> property for the <a href="https://msdn.microsoft.com/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>Receive</b> property is a Boolean value that indicates whether a specified fax port is currently receiving a fax.

This property is read-only.


## -parameters


## -remarks



To determine if a specified port is currently sending a fax, you can call the <a href="https://msdn.microsoft.com/e7759c8a-a6f3-4e42-9d56-bf93d11d7ad1">IFaxStatus::get_Send</a> method.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690310(v=VS.85).aspx">FaxStatus</a>



<a href="https://msdn.microsoft.com/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/e7759c8a-a6f3-4e42-9d56-bf93d11d7ad1">Send</a>
 

 

