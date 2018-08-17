---
UID: NF:faxcom.IFaxRoutingMethod.get_ImageName
title: IFaxRoutingMethod::get_ImageName
author: windows-sdk-content
description: The ImageName property is a null-terminated string that contains the executable image name of the fax routing extension DLL that implements the fax routing method.
old-location: fax\_mfax_ifaxroutingmethod_get_imagename_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1qud.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxRoutingMethod object [Fax Service],ImageName property, FaxRoutingMethod.ImageName, IFaxRoutingMethod.get_ImageName, IFaxRoutingMethod::get_ImageName, ImageName property [Fax Service], ImageName property [Fax Service],FaxRoutingMethod object, _mfax_ifaxroutingmethod_get_imagename, fax._mfax_ifaxroutingmethod_get_imagename, fax._mfax_ifaxroutingmethod_get_imagename_vb, get_ImageName
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

<b>ImageName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/d0b42fc6-c797-4a51-a049-240ac0566b52">ExtensionName</a>



<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/4ae5aa09-2961-4823-8c39-0b0a5b0bdc81">FaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/8dfab525-4eda-42b9-ac02-c8c25575d0aa">IFaxRoutingMethods</a>
 

 

