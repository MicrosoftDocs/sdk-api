---
UID: NF:faxcom.IFaxRoutingMethod.get_ExtensionName
title: IFaxRoutingMethod::get_ExtensionName
author: windows-sdk-content
description: The IFaxRoutingMethod::get_ExtensionName property is a null-terminated string that contains the user-friendly name for the fax routing extension DLL that implements the specified fax routing method.
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_extensionname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0e91.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ExtensionName property [Fax Service], ExtensionName property [Fax Service],IFaxRoutingMethod interface, IFaxRoutingMethod interface [Fax Service],ExtensionName property, IFaxRoutingMethod.ExtensionName, IFaxRoutingMethod.get_ExtensionName, IFaxRoutingMethod::ExtensionName, IFaxRoutingMethod::get_ExtensionName, _mfax_ifaxroutingmethod_get_extensionname, fax._mfax_ifaxroutingmethod_get_extensionname, fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_extensionname_cpp, faxcom/IFaxRoutingMethod::ExtensionName, faxcom/IFaxRoutingMethod::get_ExtensionName, get_ExtensionName
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
 - IFaxRoutingMethod.ExtensionName
 - IFaxRoutingMethod.get_ExtensionName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxRoutingMethod::get_ExtensionName


## -description


The <b>IFaxRoutingMethod::get_ExtensionName</b> property is a null-terminated string that contains the user-friendly name for the fax routing extension DLL that implements the specified fax routing method.

This property is read-only.


## -parameters


## -remarks



A fax client application can use the <a href="https://msdn.microsoft.com/c8570861-8610-4623-82bc-331492fa7dde">IFaxRoutingMethod::get_ImageName</a> property to uniquely identify the fax routing extension DLL that exports a fax routing method. Note that it is possible for multiple routing extensions to have the same user-friendly name.

<b>IFaxRoutingMethod::get_ExtensionName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/c8570861-8610-4623-82bc-331492fa7dde">IFaxRoutingMethod::get_ImageName</a>



<a href="https://msdn.microsoft.com/8dfab525-4eda-42b9-ac02-c8c25575d0aa">IFaxRoutingMethods</a>
 

 

