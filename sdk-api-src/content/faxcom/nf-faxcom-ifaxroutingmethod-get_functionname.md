---
UID: NF:faxcom.IFaxRoutingMethod.get_FunctionName
title: IFaxRoutingMethod::get_FunctionName
author: windows-sdk-content
description: The FunctionName property is a null-terminated string that contains the name of the function that executes a specific fax routing procedure.
old-location: fax\_mfax_ifaxroutingmethod_get_functionname_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1i5h.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxRoutingMethod object [Fax Service],FunctionName property, FaxRoutingMethod.FunctionName, FunctionName property [Fax Service], FunctionName property [Fax Service],FaxRoutingMethod object, IFaxRoutingMethod.get_FunctionName, IFaxRoutingMethod::get_FunctionName, _mfax_ifaxroutingmethod_get_functionname, fax._mfax_ifaxroutingmethod_get_functionname, fax._mfax_ifaxroutingmethod_get_functionname_vb, get_FunctionName
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
 - FaxRoutingMethod.FunctionName
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRoutingMethod::get_FunctionName


## -description


The <b>FunctionName</b> property is a null-terminated string that contains the name of the function that executes a specific fax routing procedure.


This property is read-only.


## -parameters


## -remarks



A fax client application can use the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">Guid</a> property to uniquely identify a fax routing method. It is possible for multiple routing methods to have the same user-friendly name and even the same function name. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691955(v=VS.85).aspx">Fax Routing Methods</a>.

<b>FunctionName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692857(v=VS.85).aspx">FaxRouteMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690703(v=VS.85).aspx">FaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692373(v=VS.85).aspx">FriendlyName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>
 

 

