---
UID: NN:faxcomex.IFaxInboundRoutingMethods
title: IFaxInboundRoutingMethods (faxcomex.h)
description: The IFaxInboundRoutingMethods interface defines a configuration collection used by a fax client application to manage the ordered inbound fax routing methods.
helpviewer_keywords: ["IFaxInboundRoutingMethods","IFaxInboundRoutingMethods interface [Fax Service]","IFaxInboundRoutingMethods interface [Fax Service]","described","_mfax_faxinboundroutingmethods_cpp","fax._mfax_faxinboundroutingmethods_cpp","faxcomex/IFaxInboundRoutingMethods"]
old-location: fax\_mfax_faxinboundroutingmethods_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_6bn7_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxInboundRoutingMethods, IFaxInboundRoutingMethods interface [Fax Service], IFaxInboundRoutingMethods interface [Fax Service],described, _mfax_faxinboundroutingmethods_cpp, fax._mfax_faxinboundroutingmethods_cpp, faxcomex/IFaxInboundRoutingMethods
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxInboundRoutingMethods
 - faxcomex/IFaxInboundRoutingMethods
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxInboundRoutingMethods
---

# IFaxInboundRoutingMethods interface


## -description

The <b>IFaxInboundRoutingMethods</b> interface defines a configuration collection used by a fax client application to manage the ordered inbound fax routing methods.

## -inheritance

The <b>IFaxInboundRoutingMethods</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxInboundRoutingMethods</b> also has these types of members:

## -remarks

Each inbound routing method is represented by a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingmethod">IFaxInboundRoutingMethod</a> interface. The order of the routing methods in the collection determines the relative order in which the methods execute when an inbound fax requires routing.

A default implementation of <b>IFaxInboundRoutingMethods</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethods">FaxInboundRoutingMethods</a> object.
