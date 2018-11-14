---
UID: NF:faxcom.IFaxRoutingMethod.get_FriendlyName
title: IFaxRoutingMethod::get_FriendlyName
author: windows-sdk-content
description: The IFaxRoutingMethod::get_FriendlyName property is a null-terminated string that contains the user-friendly name for a fax routing method.
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_friendlyname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8cdh.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
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
- apiref
: 
- COM
: 
- faxcom.h
: 
- IFaxRoutingMethod.get_FriendlyName
: 
---

# IFaxRoutingMethod::get_FriendlyName


## -description


The <b>IFaxRoutingMethod::get_FriendlyName</b> property is a null-terminated string that contains the user-friendly name for a fax routing method. 

This property is read-only.


## -parameters


## -remarks



A fax client application can use the <a href="https://msdn.microsoft.com/a87834ee-be7c-4ffc-9482-177e96bfebd0">IFaxRoutingMethod::get_Guid</a> property to uniquely identify a fax routing method. Note that it is possible for multiple routing methods to have the same user-friendly name, and even the same function name. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691955(v=VS.85).aspx">Fax Routing Methods</a>.

<b>IFaxRoutingMethod::get_FriendlyName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692857(v=VS.85).aspx">FaxRouteMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/0a6798a7-3017-4a47-a288-91a1ae453e7f">IFaxRoutingMethod::get_FunctionName</a>



<a href="https://msdn.microsoft.com/a87834ee-be7c-4ffc-9482-177e96bfebd0">IFaxRoutingMethod::get_Guid</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>
 

 

