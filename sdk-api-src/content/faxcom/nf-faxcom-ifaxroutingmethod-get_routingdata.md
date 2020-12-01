---
UID: NF:faxcom.IFaxRoutingMethod.get_RoutingData
title: IFaxRoutingMethod::get_RoutingData (faxcom.h)
description: The IFaxRoutingMethod::get_RoutingData property is a null-terminated string that contains the routing string for an incoming fax transmission.
helpviewer_keywords: ["IFaxRoutingMethod interface [Fax Service]","RoutingData property","IFaxRoutingMethod.RoutingData","IFaxRoutingMethod.get_RoutingData","IFaxRoutingMethod::RoutingData","IFaxRoutingMethod::get_RoutingData","RoutingData property [Fax Service]","RoutingData property [Fax Service]","IFaxRoutingMethod interface","_mfax_ifaxroutingmethod_get_routingdata","fax._mfax_ifaxroutingmethod_get_routingdata","fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_routingdata_cpp","faxcom/IFaxRoutingMethod::RoutingData","faxcom/IFaxRoutingMethod::get_RoutingData","get_RoutingData"]
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_routingdata_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_700x.htm
ms.date: 12/05/2018
ms.keywords: IFaxRoutingMethod interface [Fax Service],RoutingData property, IFaxRoutingMethod.RoutingData, IFaxRoutingMethod.get_RoutingData, IFaxRoutingMethod::RoutingData, IFaxRoutingMethod::get_RoutingData, RoutingData property [Fax Service], RoutingData property [Fax Service],IFaxRoutingMethod interface, _mfax_ifaxroutingmethod_get_routingdata, fax._mfax_ifaxroutingmethod_get_routingdata, fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_routingdata_cpp, faxcom/IFaxRoutingMethod::RoutingData, faxcom/IFaxRoutingMethod::get_RoutingData, get_RoutingData
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
 - IFaxRoutingMethod::get_RoutingData
 - faxcom/IFaxRoutingMethod::get_RoutingData
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
 - IFaxRoutingMethod.RoutingData
 - IFaxRoutingMethod.get_RoutingData
---

# IFaxRoutingMethod::get_RoutingData


## -description

The <b>IFaxRoutingMethod::get_RoutingData</b> property is a null-terminated string that contains the routing string for an incoming fax transmission.

This property is read-only.

## -parameters

## -remarks

<b>IFaxRoutingMethod::get_RoutingData</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethod">IFaxRoutingMethod</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethods">IFaxRoutingMethods</a>