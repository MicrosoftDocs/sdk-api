---
UID: NF:faxcom.IFaxRoutingMethod.get_RoutingData
title: IFaxRoutingMethod::get_RoutingData
author: windows-sdk-content
description: The IFaxRoutingMethod::get_RoutingData property is a null-terminated string that contains the routing string for an incoming fax transmission.
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_routingdata_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_700x.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IFaxRoutingMethod interface [Fax Service],RoutingData property, IFaxRoutingMethod.RoutingData, IFaxRoutingMethod.get_RoutingData, IFaxRoutingMethod::RoutingData, IFaxRoutingMethod::get_RoutingData, RoutingData property [Fax Service], RoutingData property [Fax Service],IFaxRoutingMethod interface, _mfax_ifaxroutingmethod_get_routingdata, fax._mfax_ifaxroutingmethod_get_routingdata, fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_routingdata_cpp, faxcom/IFaxRoutingMethod::RoutingData, faxcom/IFaxRoutingMethod::get_RoutingData, get_RoutingData
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
 - IFaxRoutingMethod.RoutingData
 - IFaxRoutingMethod.get_RoutingData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxRoutingMethod::get_RoutingData


## -description


The <b>IFaxRoutingMethod::get_RoutingData</b> property is a null-terminated string that contains the routing string for an incoming fax transmission.

This property is read-only.


## -parameters


## -remarks



<b>IFaxRoutingMethod::get_RoutingData</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>
 

 

