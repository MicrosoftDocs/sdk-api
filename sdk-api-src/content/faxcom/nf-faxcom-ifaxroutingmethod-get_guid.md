---
UID: NF:faxcom.IFaxRoutingMethod.get_Guid
title: IFaxRoutingMethod::get_Guid (faxcom.h)
author: windows-sdk-content
description: The IFaxRoutingMethod::get_Guid property is a null-terminated string that contains the GUID that uniquely identifies the fax routing method.
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_guid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1les.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Guid property [Fax Service], Guid property [Fax Service],IFaxRoutingMethod interface, IFaxRoutingMethod interface [Fax Service],Guid property, IFaxRoutingMethod.Guid, IFaxRoutingMethod.get_Guid, IFaxRoutingMethod::Guid, IFaxRoutingMethod::get_Guid, _mfax_ifaxroutingmethod_get_guid, fax._mfax_ifaxroutingmethod_get_guid, fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_guid_cpp, faxcom/IFaxRoutingMethod::Guid, faxcom/IFaxRoutingMethod::get_Guid, get_Guid
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
 - IFaxRoutingMethod.Guid
 - IFaxRoutingMethod.get_Guid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxRoutingMethod::get_Guid


## -description


The <b>IFaxRoutingMethod::get_Guid</b> property is a null-terminated string that contains the GUID that uniquely identifies the fax routing method.


This property is read-only.


## -parameters


## -remarks



A fax client application can use the <b>IFaxRoutingMethod::get_Guid</b> property to uniquely identify a fax routing method. It is possible for multiple routing methods to have the same user-friendly name, and even the same function name. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691955(v=VS.85).aspx">Fax Routing Methods</a>.

<b>IFaxRoutingMethod::get_Guid</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692373(v=VS.85).aspx">IFaxRoutingMethod::get_FriendlyName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690894(v=VS.85).aspx">IFaxRoutingMethod::get_FunctionName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>
 

 

