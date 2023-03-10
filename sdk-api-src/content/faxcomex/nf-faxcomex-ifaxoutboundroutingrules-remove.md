---
UID: NF:faxcomex.IFaxOutboundRoutingRules.Remove
title: IFaxOutboundRoutingRules::Remove (faxcomex.h)
description: The IFaxOutboundRoutingRules::Remove method removes an outbound routing rule (FaxOutboundRoutingRule object) from the FaxOutboundRoutingRules collection using the routing rule's index.
helpviewer_keywords: ["IFaxOutboundRoutingRules interface [Fax Service]","Remove method","IFaxOutboundRoutingRules.Remove","IFaxOutboundRoutingRules::Remove","Remove","Remove method [Fax Service]","Remove method [Fax Service]","IFaxOutboundRoutingRules interface","_mfax_faxoutboundroutingrules.remove","fax._mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_remove_cpp","fax._mfax_faxoutboundroutingrules_remove","faxcomex/IFaxOutboundRoutingRules::Remove"]
old-location: fax\_mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_remove_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7bs5.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutboundRoutingRules interface [Fax Service],Remove method, IFaxOutboundRoutingRules.Remove, IFaxOutboundRoutingRules::Remove, Remove, Remove method [Fax Service], Remove method [Fax Service],IFaxOutboundRoutingRules interface, _mfax_faxoutboundroutingrules.remove, fax._mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_remove_cpp, fax._mfax_faxoutboundroutingrules_remove, faxcomex/IFaxOutboundRoutingRules::Remove
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
 - IFaxOutboundRoutingRules::Remove
 - faxcomex/IFaxOutboundRoutingRules::Remove
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
 - IFaxOutboundRoutingRules.Remove
 - IFaxOutboundRoutingRules.Remove
---

# IFaxOutboundRoutingRules::Remove


## -description

The <b>IFaxOutboundRoutingRules::Remove</b> method removes an outbound routing rule (<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule">FaxOutboundRoutingRule</a> object) from the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules">FaxOutboundRoutingRules</a> collection using the routing rule's index.

## -parameters

### -param lIndex

Type: <b>long</b>

A <b>long</b> value that specifies the index of the outbound routing rule to remove from the collection. Valid values for this parameter are in the range from 1 to n, where n is the number of rules returned by a call to the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules-count-vb">IFaxOutboundRoutingRules::get_Count</a> method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The default outbound routing rule cannot be removed.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules">FaxOutboundRoutingRules</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrules">IFaxOutboundRoutingRules</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-creating-and-managing-outbound-routing-rules">Visual Basic Example</a>