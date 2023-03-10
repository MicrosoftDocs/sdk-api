---
UID: NF:faxcom.IFaxRoutingMethod.get_Enable
title: IFaxRoutingMethod::get_Enable (faxcom.h)
description: The IFaxRoutingMethod::get_Enable property is a Boolean value that indicates whether a fax routing method is enabled on a particular fax port. (Get)
helpviewer_keywords: ["Enable property [Fax Service]","Enable property [Fax Service]","IFaxRoutingMethod interface","IFaxRoutingMethod interface [Fax Service]","Enable property","IFaxRoutingMethod.Enable","IFaxRoutingMethod.get_Enable","IFaxRoutingMethod::Enable","IFaxRoutingMethod::get_Enable","IFaxRoutingMethod::put_Enable","_mfax_ifaxroutingmethod_get_enable","fax._mfax_ifaxroutingmethod_get_enable","fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_enable_cpp","faxcom/IFaxRoutingMethod::Enable","faxcom/IFaxRoutingMethod::get_Enable","faxcom/IFaxRoutingMethod::put_Enable","get_Enable"]
old-location: fax\_mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_enable_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1vmt.htm
ms.date: 12/05/2018
ms.keywords: Enable property [Fax Service], Enable property [Fax Service],IFaxRoutingMethod interface, IFaxRoutingMethod interface [Fax Service],Enable property, IFaxRoutingMethod.Enable, IFaxRoutingMethod.get_Enable, IFaxRoutingMethod::Enable, IFaxRoutingMethod::get_Enable, IFaxRoutingMethod::put_Enable, _mfax_ifaxroutingmethod_get_enable, fax._mfax_ifaxroutingmethod_get_enable, fax._mfax_ifaxroutingmethod_mfax_ifaxroutingmethod_get_enable_cpp, faxcom/IFaxRoutingMethod::Enable, faxcom/IFaxRoutingMethod::get_Enable, faxcom/IFaxRoutingMethod::put_Enable, get_Enable
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
 - IFaxRoutingMethod::get_Enable
 - faxcom/IFaxRoutingMethod::get_Enable
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
 - IFaxRoutingMethod.Enable
 - IFaxRoutingMethod.get_Enable
 - IFaxRoutingMethod.put_Enable
---

# IFaxRoutingMethod::get_Enable


## -description

The <b>IFaxRoutingMethod::get_Enable</b> property is a Boolean value that indicates whether a fax routing method is enabled on a particular fax port.


This property is read/write.

## -parameters

## -remarks

If a fax client application passes a value of <b>TRUE</b> to the <b>IFaxRoutingMethod::get_Enable</b> property, the property enables the routing method for inbound faxes on the parent port.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxport-get-canmodify-vb">CanModify</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethod">IFaxRoutingMethod</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxroutingmethods">IFaxRoutingMethods</a>
