---
UID: NF:faxcom.IFaxRoutingMethod.get_FriendlyName
title: IFaxRoutingMethod::get_FriendlyName (faxcom.h)
description: The IFaxRoutingMethod::get_FriendlyName property is a null-terminated string that contains the user-friendly name for a fax routing method.
helpviewer_keywords: ["FriendlyName property [Fax Service]","FriendlyName property [Fax Service]","IFaxRoutingMethod interface","IFaxRoutingMethod interface [Fax Service]","FriendlyName property","IFaxRoutingMethod.FriendlyName","IFaxRoutingMethod.get_FriendlyName","IFaxRoutingMethod::FriendlyName","IFaxRoutingMethod::get_FriendlyName","_mfax_ifaxroutingmethod_get_friendlyname","fax._mfax_ifaxroutingmethod_get_friendlyname","fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_friendlyname_cpp","faxcom/IFaxRoutingMethod::FriendlyName","faxcom/IFaxRoutingMethod::get_FriendlyName","get_FriendlyName"]
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_friendlyname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8cdh.htm
ms.date: 12/05/2018
ms.keywords: FriendlyName property [Fax Service], FriendlyName property [Fax Service],IFaxRoutingMethod interface, IFaxRoutingMethod interface [Fax Service],FriendlyName property, IFaxRoutingMethod.FriendlyName, IFaxRoutingMethod.get_FriendlyName, IFaxRoutingMethod::FriendlyName, IFaxRoutingMethod::get_FriendlyName, _mfax_ifaxroutingmethod_get_friendlyname, fax._mfax_ifaxroutingmethod_get_friendlyname, fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_friendlyname_cpp, faxcom/IFaxRoutingMethod::FriendlyName, faxcom/IFaxRoutingMethod::get_FriendlyName, get_FriendlyName
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
 - IFaxRoutingMethod::get_FriendlyName
 - faxcom/IFaxRoutingMethod::get_FriendlyName
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
 - IFaxRoutingMethod.FriendlyName
 - IFaxRoutingMethod.get_FriendlyName
---

# IFaxRoutingMethod::get_FriendlyName


## -description

The <b>IFaxRoutingMethod::get_FriendlyName</b> property is a null-terminated string that contains the user-friendly name for a fax routing method. 

This property is read-only.

## -parameters

## -remarks

A fax client application can use the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxroutingmethod-get-guid-vb">IFaxRoutingMethod::get_Guid</a> property to uniquely identify a fax routing method. Note that it is possible for multiple routing methods to have the same user-friendly name, and even the same function name. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-methods">Fax Routing Methods</a>.

<b>IFaxRoutingMethod::get_FriendlyName</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/windows/desktop/api/faxroute/nc-faxroute-pfaxroutemethod">FaxRouteMethod</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethod">IFaxRoutingMethod</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxroutingmethod-get-functionname-vb">IFaxRoutingMethod::get_FunctionName</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxroutingmethod-get-guid-vb">IFaxRoutingMethod::get_Guid</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethods">IFaxRoutingMethods</a>