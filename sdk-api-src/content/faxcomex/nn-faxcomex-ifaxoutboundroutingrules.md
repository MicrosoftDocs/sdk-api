---
UID: NN:faxcomex.IFaxOutboundRoutingRules
title: IFaxOutboundRoutingRules (faxcomex.h)
description: The IFaxOutboundRoutingRules interface describes a configuration collection that is used by a fax client application to manage the fax outbound routing rules.
helpviewer_keywords: ["IFaxOutboundRoutingRules","IFaxOutboundRoutingRules interface [Fax Service]","IFaxOutboundRoutingRules interface [Fax Service]","described","_mfax_faxoutboundroutingrules_cpp","fax._mfax_faxoutboundroutingrules_cpp","faxcomex/IFaxOutboundRoutingRules"]
old-location: fax\_mfax_faxoutboundroutingrules_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_69f7_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutboundRoutingRules, IFaxOutboundRoutingRules interface [Fax Service], IFaxOutboundRoutingRules interface [Fax Service],described, _mfax_faxoutboundroutingrules_cpp, fax._mfax_faxoutboundroutingrules_cpp, faxcomex/IFaxOutboundRoutingRules
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
 - IFaxOutboundRoutingRules
 - faxcomex/IFaxOutboundRoutingRules
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
 - IFaxOutboundRoutingRules
---

# IFaxOutboundRoutingRules interface


## -description

The <b>IFaxOutboundRoutingRules</b> interface describes a configuration collection that is used by a fax client application to manage the fax outbound routing rules. The collection also includes methods to add and remove rules from the collection. Each outbound routing rule is represented by a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a> interface.

## -inheritance

The <b>IFaxOutboundRoutingRules</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxOutboundRoutingRules</b> also has these types of members:

## -remarks

A default implementation of <b>IFaxOutboundRoutingRules</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules">FaxOutboundRoutingRules</a> object.
