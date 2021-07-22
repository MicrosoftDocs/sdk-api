---
UID: NF:faxcomex.IFaxOutboundRoutingRules.RemoveByCountryAndArea
title: IFaxOutboundRoutingRules::RemoveByCountryAndArea (faxcomex.h)
description: The IFaxOutboundRoutingRules::RemoveByCountryAndArea method removes an outbound routing rule (FaxOutboundRoutingRule object) from the collection using the routing rule's country/region code and area code.
helpviewer_keywords: ["IFaxOutboundRoutingRules interface [Fax Service]","RemoveByCountryAndArea method","IFaxOutboundRoutingRules.RemoveByCountryAndArea","IFaxOutboundRoutingRules::RemoveByCountryAndArea","RemoveByCountryAndArea","RemoveByCountryAndArea method [Fax Service]","RemoveByCountryAndArea method [Fax Service]","IFaxOutboundRoutingRules interface","_mfax_faxoutboundroutingrules.removebycountryandarea","fax._mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_removebycountryandarea_cpp","fax._mfax_faxoutboundroutingrules_removebycountryandarea","faxcomex/IFaxOutboundRoutingRules::RemoveByCountryAndArea"]
old-location: fax\_mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_removebycountryandarea_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_62e9.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutboundRoutingRules interface [Fax Service],RemoveByCountryAndArea method, IFaxOutboundRoutingRules.RemoveByCountryAndArea, IFaxOutboundRoutingRules::RemoveByCountryAndArea, RemoveByCountryAndArea, RemoveByCountryAndArea method [Fax Service], RemoveByCountryAndArea method [Fax Service],IFaxOutboundRoutingRules interface, _mfax_faxoutboundroutingrules.removebycountryandarea, fax._mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_removebycountryandarea_cpp, fax._mfax_faxoutboundroutingrules_removebycountryandarea, faxcomex/IFaxOutboundRoutingRules::RemoveByCountryAndArea
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
 - IFaxOutboundRoutingRules::RemoveByCountryAndArea
 - faxcomex/IFaxOutboundRoutingRules::RemoveByCountryAndArea
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
 - IFaxOutboundRoutingRules.RemoveByCountryAndArea
 - IFaxOutboundRoutingRules.RemoveByCountryAndArea
---

# IFaxOutboundRoutingRules::RemoveByCountryAndArea


## -description

The <b>IFaxOutboundRoutingRules::RemoveByCountryAndArea</b> method removes an outbound routing rule (<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule">FaxOutboundRoutingRule</a> object) from the collection using the routing rule's country/region code and area code.

## -parameters

### -param lCountryCode

Type: <b>long</b>

A <b>long</b> value that specifies the country/region code of the outbound routing rule to remove from the collection. Specifying <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_routing_rule_code_enum">frrcANY_CODE</a> will remove a rule that applies to all country/region codes.

### -param lAreaCode

Type: <b>long</b>

A <b>long</b> value that specifies the area code of the outbound routing rule to remove from the collection. Specifying <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_routing_rule_code_enum">frrcANY_CODE</a> will remove a rule that applies to all area codes within the specified country/region code.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You cannot set both <i>lCountryCode</i> and <i>lAreaCode</i> to <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_routing_rule_code_enum">frrcANY_CODE</a> because this is equivalent to specifying the default outbound routing rule, which cannot be removed.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules">FaxOutboundRoutingRules</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrules">IFaxOutboundRoutingRules</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-creating-and-managing-outbound-routing-rules">Visual Basic Example</a>