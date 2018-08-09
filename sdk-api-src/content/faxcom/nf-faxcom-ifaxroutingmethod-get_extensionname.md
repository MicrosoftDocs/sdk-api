---
UID: NF:faxcom.IFaxRoutingMethod.get_ExtensionName
title: IFaxRoutingMethod::get_ExtensionName
author: windows-sdk-content
description: The ExtensionName property is a null-terminated string that contains the user-friendly name for the fax routing extension DLL that implements the specified fax routing method.
old-location: fax\_mfax_ifaxroutingmethod_get_extensionname_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0e91.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ExtensionName property [Fax Service], ExtensionName property [Fax Service],FaxRoutingMethod object, FaxRoutingMethod object [Fax Service],ExtensionName property, FaxRoutingMethod.ExtensionName, IFaxRoutingMethod.get_ExtensionName, IFaxRoutingMethod::get_ExtensionName, _mfax_ifaxroutingmethod_get_extensionname, fax._mfax_ifaxroutingmethod_get_extensionname, fax._mfax_ifaxroutingmethod_get_extensionname_vb, get_ExtensionName
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
 - FaxRoutingMethod.ExtensionName
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRoutingMethod::get_ExtensionName


## -description


The <b>ExtensionName</b> property is a null-terminated string that contains the user-friendly name for the fax routing extension DLL that implements the specified fax routing method.

This property is read-only.


## -parameters


## -remarks



A fax client application can use the <a href="https://msdn.microsoft.com/library/windows/hardware/dn895612">ImageName</a> property to uniquely identify the fax routing extension DLL that exports a fax routing method. Note that it is possible for multiple routing extensions to have the same user-friendly name.

<b>ExtensionName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690703(v=VS.85).aspx">FaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn895612">ImageName</a>
 

 

