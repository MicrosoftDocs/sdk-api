---
UID: NF:faxcom.IFaxPort.GetRoutingMethods
title: IFaxPort::GetRoutingMethods
author: windows-sdk-content
description: The GetRoutingMethods interface method creates a FaxRoutingMethods object for the parent FaxPort object.
old-location: fax\_mfax_ifaxport_getroutingmethods_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_619v.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: FaxPort object [Fax Service],GetRoutingMethods method, FaxPort.GetRoutingMethods, GetRoutingMethods, GetRoutingMethods method [Fax Service], GetRoutingMethods method [Fax Service],FaxPort object, IFaxPort.GetRoutingMethods, IFaxPort::GetRoutingMethods, _mfax_ifaxport_getroutingmethods, fax._mfax_ifaxport_getroutingmethods, fax._mfax_ifaxport_getroutingmethods_vb
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
 - FaxPort.GetRoutingMethods
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxPort::GetRoutingMethods


## -description


The <b>GetRoutingMethods</b> interface method creates a <a href="https://msdn.microsoft.com/library/ms692847(v=VS.85).aspx">FaxRoutingMethods</a> object for the parent <a href="https://msdn.microsoft.com/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The FaxRoutingMethods object allows enumeration of the fax routing methods associated with a fax port. Fax routing methods are defined by a fax routing extension DLL.


## -parameters




### -param retval






#### - retVal [out]

Type: <b><a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>*</b>

Retrieves a <a href="https://msdn.microsoft.com/library/ms692847(v=VS.85).aspx">FaxRoutingMethods</a> object.


## -remarks



The <b>GetRoutingMethods</b> interface method retrieves an <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/library/ms692847(v=VS.85).aspx">FaxRoutingMethods</a> object. This object is derived from the <a href="https://msdn.microsoft.com/library/ms691338(v=VS.85).aspx">FaxPort</a> object specified by the <a href="https://msdn.microsoft.com/library/ms690893(v=VS.85).aspx">IFaxPorts</a> interface.

A fax client application can access the <a href="https://msdn.microsoft.com/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a> interface directly by calling the <a href="https://msdn.microsoft.com/library/Dd757101(v=VS.85).aspx">IUnknown::QueryInterface</a> method to retrieve an interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690315(v=VS.85).aspx">FaxPort</a>



<a href="https://msdn.microsoft.com/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>
 

 

