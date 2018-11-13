---
UID: NF:faxcom.IFaxRoutingMethod.get_ImageName
title: IFaxRoutingMethod::get_ImageName
author: windows-sdk-content
description: The IFaxRoutingMethod::get_ImageName property is a null-terminated string that contains the executable image name of the fax routing extension DLL that implements the fax routing method.
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_imagename_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1qud.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxRoutingMethod interface [Fax Service],ImageName property, IFaxRoutingMethod.ImageName, IFaxRoutingMethod.get_ImageName, IFaxRoutingMethod::ImageName, IFaxRoutingMethod::get_ImageName, ImageName property [Fax Service], ImageName property [Fax Service],IFaxRoutingMethod interface, _mfax_ifaxroutingmethod_get_imagename, fax._mfax_ifaxroutingmethod_get_imagename, fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_imagename_cpp, faxcom/IFaxRoutingMethod::ImageName, faxcom/IFaxRoutingMethod::get_ImageName, get_ImageName
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
 - IFaxRoutingMethod.ImageName
 - IFaxRoutingMethod.get_ImageName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxRoutingMethod::get_ImageName


## -description


The <b>IFaxRoutingMethod::get_ImageName</b> property is a null-terminated string that contains the executable image name of the fax routing extension DLL that implements the fax routing method.

This property is read-only.


## -parameters


## -remarks



A fax client application can use the <b>IFaxRoutingMethod::get_ImageName</b> property to uniquely identify the fax routing extension DLL that exports a fax routing method. Note that it is possible for multiple routing extensions to have the same user-friendly name.

<b>IFaxRoutingMethod::get_ImageName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/a205f9f6-719e-4520-b8ee-0e303b6c5113">IFaxRoutingMethod::get_ExtensionName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>
 

 

