---
UID: NF:faxcom.IFaxRoutingMethod.get_Guid
title: IFaxRoutingMethod::get_Guid
author: windows-driver-content
description: The Guid property is a null-terminated string that contains the GUID that uniquely identifies the fax routing method.
old-location: fax\_mfax_ifaxroutingmethod_get_guid_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1les.htm
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: FaxRoutingMethod object [Fax Service],Guid property, FaxRoutingMethod.Guid, Guid property [Fax Service], Guid property [Fax Service],FaxRoutingMethod object, IFaxRoutingMethod.get_Guid, IFaxRoutingMethod::get_Guid, _mfax_ifaxroutingmethod_get_guid, fax._mfax_ifaxroutingmethod_get_guid, fax._mfax_ifaxroutingmethod_get_guid_vb, get_Guid
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
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Faxcom.dll
api_name:
-	FaxRoutingMethod.Guid
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRoutingMethod::get_Guid


## -description


The <b>Guid</b> property is a null-terminated string that contains the GUID that uniquely identifies the fax routing method.


This property is read-only.


## -parameters


## -remarks



A fax client application can use the <b>Guid</b> property to uniquely identify a fax routing method. It is possible for multiple routing methods to have the same user-friendly name, and even the same function name. For more information, see <a href="https://msdn.microsoft.com/a2144af9-9101-478f-93b9-393101dc1936">Fax Routing Methods</a>.

<b>Guid</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/4ae5aa09-2961-4823-8c39-0b0a5b0bdc81">FaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/9fdcc223-f919-4e55-af89-4734888fdbf7">FriendlyName</a>



<a href="https://msdn.microsoft.com/144023b3-bf12-4e81-856c-6745695d9c30">FunctionName</a>



<a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/8dfab525-4eda-42b9-ac02-c8c25575d0aa">IFaxRoutingMethods</a>
 

 

