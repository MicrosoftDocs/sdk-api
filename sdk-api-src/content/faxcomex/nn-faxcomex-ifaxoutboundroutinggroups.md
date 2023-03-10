---
UID: NN:faxcomex.IFaxOutboundRoutingGroups
title: IFaxOutboundRoutingGroups (faxcomex.h)
description: The IFaxOutboundRoutingGroups interface describes a configuration collection used by a fax client application to manage the fax outbound routing groups, represented by IFaxOutboundRoutingGroup interfaces.
helpviewer_keywords: ["IFaxOutboundRoutingGroups","IFaxOutboundRoutingGroups interface [Fax Service]","IFaxOutboundRoutingGroups interface [Fax Service]","described","_mfax_faxoutboundroutinggroups_cpp","fax._mfax_faxoutboundroutinggroups_cpp","faxcomex/IFaxOutboundRoutingGroups"]
old-location: fax\_mfax_faxoutboundroutinggroups_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_62r7_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutboundRoutingGroups, IFaxOutboundRoutingGroups interface [Fax Service], IFaxOutboundRoutingGroups interface [Fax Service],described, _mfax_faxoutboundroutinggroups_cpp, fax._mfax_faxoutboundroutinggroups_cpp, faxcomex/IFaxOutboundRoutingGroups
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
 - IFaxOutboundRoutingGroups
 - faxcomex/IFaxOutboundRoutingGroups
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
 - IFaxOutboundRoutingGroups
---

# IFaxOutboundRoutingGroups interface


## -description

The <b>IFaxOutboundRoutingGroups</b> interface describes a configuration collection used by a fax client application to manage the fax outbound routing groups, represented by <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroup">IFaxOutboundRoutingGroup</a> interfaces. The interface also includes methods to add and remove groups from the collection.
<div class="alert"><b>Note</b>  The outbound routing group <b>All Devices</b> is always the first object in this collection. You cannot remove the <b>All Devices</b> group from the collection. If you attempt to remove it, you will receive an error message.
</div><div> </div>

## -inheritance

The <b>IFaxOutboundRoutingGroups</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxOutboundRoutingGroups</b> also has these types of members:

## -remarks

A default implementation of <b>IFaxOutboundRoutingGroups</b> is provided as the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutinggroups">FaxOutboundRoutingGroups</a> object.
