---
UID: NF:faxcom.IFaxRoutingMethod.get_FunctionName
title: IFaxRoutingMethod::get_FunctionName
author: windows-sdk-content
description: The IFaxRoutingMethod::get_FunctionName property is a null-terminated string that contains the name of the function that executes a specific fax routing procedure.
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_functionname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1i5h.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FunctionName property [Fax Service], FunctionName property [Fax Service],IFaxRoutingMethod interface, IFaxRoutingMethod interface [Fax Service],FunctionName property, IFaxRoutingMethod.FunctionName, IFaxRoutingMethod.get_FunctionName, IFaxRoutingMethod::FunctionName, IFaxRoutingMethod::get_FunctionName, _mfax_ifaxroutingmethod_get_functionname, fax._mfax_ifaxroutingmethod_get_functionname, fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_functionname_cpp, faxcom/IFaxRoutingMethod::FunctionName, faxcom/IFaxRoutingMethod::get_FunctionName, get_FunctionName
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
 - IFaxRoutingMethod.FunctionName
 - IFaxRoutingMethod.get_FunctionName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxRoutingMethod::get_FunctionName


## -description


The <b>IFaxRoutingMethod::get_FunctionName</b> property is a null-terminated string that contains the name of the function that executes a specific fax routing procedure.


This property is read-only.


## -parameters


## -remarks



A fax client application can use the <a href="https://msdn.microsoft.com/a87834ee-be7c-4ffc-9482-177e96bfebd0">IFaxRoutingMethod::get_Guid</a> property to uniquely identify a fax routing method. It is possible for multiple routing methods to have the same user-friendly name and even the same function name. For more information, see <a href="https://msdn.microsoft.com/a2144af9-9101-478f-93b9-393101dc1936">Fax Routing Methods</a>.

<b>IFaxRoutingMethod::get_FunctionName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/c9220335-bb45-48b3-b303-b6ea10260952">FaxRouteMethod</a>



<a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/b2d01012-9c84-4f86-9b20-68d813f9f52a">IFaxRoutingMethod::get_FriendlyName</a>



<a href="https://msdn.microsoft.com/8dfab525-4eda-42b9-ac02-c8c25575d0aa">IFaxRoutingMethods</a>
 

 

