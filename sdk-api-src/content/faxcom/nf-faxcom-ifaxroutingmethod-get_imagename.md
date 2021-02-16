---
UID: NF:faxcom.IFaxRoutingMethod.get_ImageName
title: IFaxRoutingMethod::get_ImageName (faxcom.h)
description: The IFaxRoutingMethod::get_ImageName property is a null-terminated string that contains the executable image name of the fax routing extension DLL that implements the fax routing method.
helpviewer_keywords: ["IFaxRoutingMethod interface [Fax Service]","ImageName property","IFaxRoutingMethod.ImageName","IFaxRoutingMethod.get_ImageName","IFaxRoutingMethod::ImageName","IFaxRoutingMethod::get_ImageName","ImageName property [Fax Service]","ImageName property [Fax Service]","IFaxRoutingMethod interface","_mfax_ifaxroutingmethod_get_imagename","fax._mfax_ifaxroutingmethod_get_imagename","fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_imagename_cpp","faxcom/IFaxRoutingMethod::ImageName","faxcom/IFaxRoutingMethod::get_ImageName","get_ImageName"]
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_imagename_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1qud.htm
ms.date: 12/05/2018
ms.keywords: IFaxRoutingMethod interface [Fax Service],ImageName property, IFaxRoutingMethod.ImageName, IFaxRoutingMethod.get_ImageName, IFaxRoutingMethod::ImageName, IFaxRoutingMethod::get_ImageName, ImageName property [Fax Service], ImageName property [Fax Service],IFaxRoutingMethod interface, _mfax_ifaxroutingmethod_get_imagename, fax._mfax_ifaxroutingmethod_get_imagename, fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_imagename_cpp, faxcom/IFaxRoutingMethod::ImageName, faxcom/IFaxRoutingMethod::get_ImageName, get_ImageName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxRoutingMethod::get_ImageName
 - faxcom/IFaxRoutingMethod::get_ImageName
dev_langs:
 - c++
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
---

# IFaxRoutingMethod::get_ImageName


## -description

The <b>IFaxRoutingMethod::get_ImageName</b> property is a null-terminated string that contains the executable image name of the fax routing extension DLL that implements the fax routing method.

This property is read-only.

## -parameters

## -remarks

A fax client application can use the <b>IFaxRoutingMethod::get_ImageName</b> property to uniquely identify the fax routing extension DLL that exports a fax routing method. Note that it is possible for multiple routing extensions to have the same user-friendly name.

<b>IFaxRoutingMethod::get_ImageName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethod">IFaxRoutingMethod</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxroutingmethod-get-extensionname-vb">IFaxRoutingMethod::get_ExtensionName</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethods">IFaxRoutingMethods</a>