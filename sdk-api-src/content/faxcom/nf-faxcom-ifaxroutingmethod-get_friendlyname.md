---
UID: NF:faxcom.IFaxRoutingMethod.get_FriendlyName
title: IFaxRoutingMethod::get_FriendlyName
author: windows-sdk-content
description: The FriendlyName property is a null-terminated string that contains the user-friendly name for a fax routing method.
old-location: fax\_mfax_ifaxroutingmethod_get_friendlyname_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8cdh.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxRoutingMethod object [Fax Service],FriendlyName property, FaxRoutingMethod.FriendlyName, FriendlyName property [Fax Service], FriendlyName property [Fax Service],FaxRoutingMethod object, IFaxRoutingMethod.get_FriendlyName, IFaxRoutingMethod::get_FriendlyName, _mfax_ifaxroutingmethod_get_friendlyname, fax._mfax_ifaxroutingmethod_get_friendlyname, fax._mfax_ifaxroutingmethod_get_friendlyname_vb, get_FriendlyName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.redist: 
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
 - FaxRoutingMethod.FriendlyName
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRoutingMethod::get_FriendlyName


## -description


The <b>FriendlyName</b> property is a null-terminated string that contains the user-friendly name for a fax routing method. 

This property is read-only.


## -parameters


## -remarks



A fax client application can use the <a href="https://msdn.microsoft.com/en-us/library/ms690897(v=VS.85).aspx">Guid</a> property to uniquely identify a fax routing method. Note that it is possible for multiple routing methods to have the same user-friendly name, and even the same function name. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691955(v=VS.85).aspx">Fax Routing Methods</a>.

<b>FriendlyName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692857(v=VS.85).aspx">FaxRouteMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690703(v=VS.85).aspx">FaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690894(v=VS.85).aspx">FunctionName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690897(v=VS.85).aspx">Guid</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>
 

 

