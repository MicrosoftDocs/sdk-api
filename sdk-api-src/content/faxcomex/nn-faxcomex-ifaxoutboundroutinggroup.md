---
UID: NN:faxcomex.IFaxOutboundRoutingGroup
title: IFaxOutboundRoutingGroup (faxcomex.h)
description: The IFaxOutboundRoutingGroup interface describes a configuration object that is used by a fax client application to retrieve information about an individual fax outbound routing group.
helpviewer_keywords: ["IFaxOutboundRoutingGroup","IFaxOutboundRoutingGroup interface [Fax Service]","IFaxOutboundRoutingGroup interface [Fax Service]","described","_mfax_faxoutboundroutinggroup_cpp","fax._mfax_faxoutboundroutinggroup_cpp","faxcomex/IFaxOutboundRoutingGroup"]
old-location: fax\_mfax_faxoutboundroutinggroup_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_45o0_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutboundRoutingGroup, IFaxOutboundRoutingGroup interface [Fax Service], IFaxOutboundRoutingGroup interface [Fax Service],described, _mfax_faxoutboundroutinggroup_cpp, fax._mfax_faxoutboundroutinggroup_cpp, faxcomex/IFaxOutboundRoutingGroup
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
 - IFaxOutboundRoutingGroup
 - faxcomex/IFaxOutboundRoutingGroup
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
 - IFaxOutboundRoutingGroup
---

# IFaxOutboundRoutingGroup interface


## -description

The <b>IFaxOutboundRoutingGroup</b> interface describes a configuration object that is used by a fax client application to retrieve information about an individual fax outbound routing group. The object also includes a method to retrieve the ordered collection of device IDs (<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceids">IFaxDeviceIds</a> interfaces) that participate in the routing group. The order of the devices in the collection determines the relative order in which available devices send outgoing transmissions.

## -remarks

A default implementation of <b>IFaxOutboundRoutingGroup</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutinggroup">FaxOutboundRoutingGroup</a> object.