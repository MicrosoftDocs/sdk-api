---
UID: NF:faxcom.IFaxPort.GetRoutingMethods
title: IFaxPort::GetRoutingMethods
author: windows-sdk-content
description: The IFaxPort::GetRoutingMethods interface method creates a FaxRoutingMethods object for the parent FaxPort object.
old-location: fax\_mfax_ifaxport_mfax_ifaxport_getroutingmethods_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_619v.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
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


The <b>IFaxPort::GetRoutingMethods</b> interface method creates a <a href="https://msdn.microsoft.com/8f164bc0-647c-4495-be67-2f208770c28d">FaxRoutingMethods</a> object for the parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The FaxRoutingMethods object allows enumeration of the fax routing methods associated with a fax port. Fax routing methods are defined by a fax routing extension DLL.


## -parameters




### -param retval

TBD




#### - retVal [out]

Type: <b><a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>*</b>

Pointer to a <b>VARIANT</b> structure that receives an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/8f164bc0-647c-4495-be67-2f208770c28d">FaxRoutingMethods</a> object. The method returns a <b>ppdispVal</b> member with a VT_DISPATCH data type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>IFaxPort::GetRoutingMethods</b> interface method retrieves an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/8f164bc0-647c-4495-be67-2f208770c28d">FaxRoutingMethods</a> object. This object is derived from the <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object specified by the <a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a> interface.

A fax client application can access the <a href="https://msdn.microsoft.com/8dfab525-4eda-42b9-ac02-c8c25575d0aa">IFaxRoutingMethods</a> interface directly by calling the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>



<a href="https://msdn.microsoft.com/8dfab525-4eda-42b9-ac02-c8c25575d0aa">IFaxRoutingMethods</a>
 

 

