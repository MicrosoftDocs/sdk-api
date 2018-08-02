---
UID: NF:faxcom.IFaxRoutingMethod.get_ImageName
title: IFaxRoutingMethod::get_ImageName
author: windows-sdk-content
description: The ImageName property is a null-terminated string that contains the executable image name of the fax routing extension DLL that implements the fax routing method.
old-location: fax\_mfax_ifaxroutingmethod_get_imagename_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1qud.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FaxRoutingMethod object [Fax Service],ImageName property, FaxRoutingMethod.ImageName, IFaxRoutingMethod.get_ImageName, IFaxRoutingMethod::get_ImageName, ImageName property [Fax Service], ImageName property [Fax Service],FaxRoutingMethod object, _mfax_ifaxroutingmethod_get_imagename, fax._mfax_ifaxroutingmethod_get_imagename, fax._mfax_ifaxroutingmethod_get_imagename_vb, get_ImageName
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
 - FaxRoutingMethod.ImageName
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRoutingMethod::get_ImageName


## -description


The <b>ImageName</b> property is a null-terminated string that contains the executable image name of the fax routing extension DLL that implements the fax routing method.

This property is read-only.


## -parameters


## -remarks



A fax client application can use the <b>ImageName</b> property to uniquely identify the fax routing extension DLL that exports a fax routing method. Note that it is possible for multiple routing extensions to have the same user-friendly name.

<b>ImageName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690798(v=VS.85).aspx">ExtensionName</a>



<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690703(v=VS.85).aspx">FaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>
 

 

