---
UID: NF:faxcom.IFaxPort.GetRoutingMethods
title: IFaxPort::GetRoutingMethods
author: windows-sdk-content
description: The GetRoutingMethods interface method creates a FaxRoutingMethods object for the parent FaxPort object.
old-location: fax\_mfax_ifaxport_getroutingmethods_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_619v.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
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


The <b>GetRoutingMethods</b> interface method creates a <a href="https://msdn.microsoft.com/8f164bc0-647c-4495-be67-2f208770c28d">FaxRoutingMethods</a> object for the parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The FaxRoutingMethods object allows enumeration of the fax routing methods associated with a fax port. Fax routing methods are defined by a fax routing extension DLL.


## -parameters




### -param retval






#### - retVal [out]

Type: <b><a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>*</b>

Retrieves a <a href="https://msdn.microsoft.com/8f164bc0-647c-4495-be67-2f208770c28d">FaxRoutingMethods</a> object.


## -remarks



The <b>GetRoutingMethods</b> interface method retrieves an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/8f164bc0-647c-4495-be67-2f208770c28d">FaxRoutingMethods</a> object. This object is derived from the <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object specified by the <a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a> interface.

A fax client application can access the <a href="https://msdn.microsoft.com/8dfab525-4eda-42b9-ac02-c8c25575d0aa">IFaxRoutingMethods</a> interface directly by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a> method to retrieve an interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/7888d042-7d85-4921-b233-f6e95e0c80d9">FaxPort</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>



<a href="https://msdn.microsoft.com/8dfab525-4eda-42b9-ac02-c8c25575d0aa">IFaxRoutingMethods</a>
 

 

