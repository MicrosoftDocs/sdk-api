---
UID: NF:faxcom.IFaxPort.GetRoutingMethods
title: IFaxPort::GetRoutingMethods
author: windows-sdk-content
description: The IFaxPort::GetRoutingMethods interface method creates a FaxRoutingMethods object for the parent FaxPort object.
old-location: fax\_mfax_ifaxport_mfax_ifaxport_getroutingmethods_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_619v.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: GetRoutingMethods, GetRoutingMethods method [Fax Service], GetRoutingMethods method [Fax Service],IFaxPort interface, IFaxPort interface [Fax Service],GetRoutingMethods method, IFaxPort.GetRoutingMethods, IFaxPort::GetRoutingMethods, _mfax_ifaxport_getroutingmethods, fax._mfax_ifaxport_getroutingmethods, fax._mfax_ifaxport_mfax_ifaxport_getroutingmethods_cpp, faxcom/IFaxPort::GetRoutingMethods
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
 - IFaxPort.GetRoutingMethods
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxPort::GetRoutingMethods


## -description


The <b>IFaxPort::GetRoutingMethods</b> interface method creates a <a href="https://msdn.microsoft.com/en-us/library/ms692847(v=VS.85).aspx">FaxRoutingMethods</a> object for the parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The FaxRoutingMethods object allows enumeration of the fax routing methods associated with a fax port. Fax routing methods are defined by a fax routing extension DLL.


## -parameters




### -param retval

TBD




#### - retVal [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>*</b>

Pointer to a <b>VARIANT</b> structure that receives an <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms692847(v=VS.85).aspx">FaxRoutingMethods</a> object. The method returns a <b>ppdispVal</b> member with a VT_DISPATCH data type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>IFaxPort::GetRoutingMethods</b> interface method retrieves an <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms692847(v=VS.85).aspx">FaxRoutingMethods</a> object. This object is derived from the <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object specified by the <a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a> interface.

A fax client application can access the <a href="https://msdn.microsoft.com/en-us/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a> interface directly by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method to retrieve an interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>
 

 

