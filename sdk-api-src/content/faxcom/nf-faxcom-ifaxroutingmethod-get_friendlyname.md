---
UID: NF:faxcom.IFaxRoutingMethod.get_FriendlyName
title: IFaxRoutingMethod::get_FriendlyName
author: windows-sdk-content
description: The IFaxRoutingMethod::get_FriendlyName property is a null-terminated string that contains the user-friendly name for a fax routing method.
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_friendlyname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8cdh.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FriendlyName property [Fax Service], FriendlyName property [Fax Service],IFaxRoutingMethod interface, IFaxRoutingMethod interface [Fax Service],FriendlyName property, IFaxRoutingMethod.FriendlyName, IFaxRoutingMethod.get_FriendlyName, IFaxRoutingMethod::FriendlyName, IFaxRoutingMethod::get_FriendlyName, _mfax_ifaxroutingmethod_get_friendlyname, fax._mfax_ifaxroutingmethod_get_friendlyname, fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_friendlyname_cpp, faxcom/IFaxRoutingMethod::FriendlyName, faxcom/IFaxRoutingMethod::get_FriendlyName, get_FriendlyName
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
 - IFaxRoutingMethod.FriendlyName
 - IFaxRoutingMethod.get_FriendlyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxRoutingMethod::get_FriendlyName


## -description


The <b>IFaxRoutingMethod::get_FriendlyName</b> property is a null-terminated string that contains the user-friendly name for a fax routing method. 

This property is read-only.


## -parameters


## -remarks



A fax client application can use the <a href="https://msdn.microsoft.com/a87834ee-be7c-4ffc-9482-177e96bfebd0">IFaxRoutingMethod::get_Guid</a> property to uniquely identify a fax routing method. Note that it is possible for multiple routing methods to have the same user-friendly name, and even the same function name. For more information, see <a href="https://msdn.microsoft.com/a2144af9-9101-478f-93b9-393101dc1936">Fax Routing Methods</a>.

<b>IFaxRoutingMethod::get_FriendlyName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/c9220335-bb45-48b3-b303-b6ea10260952">FaxRouteMethod</a>



<a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/0a6798a7-3017-4a47-a288-91a1ae453e7f">IFaxRoutingMethod::get_FunctionName</a>



<a href="https://msdn.microsoft.com/a87834ee-be7c-4ffc-9482-177e96bfebd0">IFaxRoutingMethod::get_Guid</a>



<a href="https://msdn.microsoft.com/8dfab525-4eda-42b9-ac02-c8c25575d0aa">IFaxRoutingMethods</a>
 

 

