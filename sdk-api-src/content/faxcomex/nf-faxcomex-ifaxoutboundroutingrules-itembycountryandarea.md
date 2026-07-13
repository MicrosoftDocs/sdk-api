---
UID: NF:faxcomex.IFaxOutboundRoutingRules.ItemByCountryAndArea
title: IFaxOutboundRoutingRules::ItemByCountryAndArea (faxcomex.h)
description: The IFaxOutboundRoutingRules::get_ItemByCountryAndArea method returns an outbound routing rule (FaxOutboundRoutingRule object) from the collection using the routing rule's country/region code and area code.
helpviewer_keywords: ["IFaxOutboundRoutingRules interface [Fax Service]","ItemByCountryAndArea method","IFaxOutboundRoutingRules.ItemByCountryAndArea","IFaxOutboundRoutingRules::ItemByCountryAndArea","ItemByCountryAndArea","ItemByCountryAndArea method [Fax Service]","ItemByCountryAndArea method [Fax Service]","IFaxOutboundRoutingRules interface","_mfax_faxoutboundroutingrules.itembycountryandarea","fax._mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_itembycountryandarea_cpp","fax._mfax_faxoutboundroutingrules_itembycountryandarea","faxcomex/IFaxOutboundRoutingRules::ItemByCountryAndArea"]
old-location: fax\_mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_itembycountryandarea_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8plt.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutboundRoutingRules interface [Fax Service],ItemByCountryAndArea method, IFaxOutboundRoutingRules.ItemByCountryAndArea, IFaxOutboundRoutingRules::ItemByCountryAndArea, ItemByCountryAndArea, ItemByCountryAndArea method [Fax Service], ItemByCountryAndArea method [Fax Service],IFaxOutboundRoutingRules interface, _mfax_faxoutboundroutingrules.itembycountryandarea, fax._mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_itembycountryandarea_cpp, fax._mfax_faxoutboundroutingrules_itembycountryandarea, faxcomex/IFaxOutboundRoutingRules::ItemByCountryAndArea
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
 - IFaxOutboundRoutingRules::ItemByCountryAndArea
 - faxcomex/IFaxOutboundRoutingRules::ItemByCountryAndArea
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
 - IFaxOutboundRoutingRules.ItemByCountryAndArea
---

## -description

The <b>IFaxOutboundRoutingRules::get_ItemByCountryAndArea</b> method returns an outbound routing rule (<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule">FaxOutboundRoutingRule</a> object) from the collection using the routing rule's country/region code and area code.

## -parameters

### -param lCountryCode

Type: <b>long</b>

A <b>long</b> value that specifies the country/region code of the outbound routing rule to retrieve. Specifying <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_routing_rule_code_enum">frrcANY_CODE</a> will return a rule for any country/region code.

### -param lAreaCode

Type: <b>long</b>

A <b>long</b> value that specifies the area code of the outbound routing rule to retrieve. Specifying <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_routing_rule_code_enum">frrcANY_CODE</a> will return a rule for any area code within the specified country/region code.

### -param pFaxOutboundRoutingRule

Type: <b><a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule">FaxOutboundRoutingRule</a>**</b>

A <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule">FaxOutboundRoutingRule</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules">FaxOutboundRoutingRules</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrules">IFaxOutboundRoutingRules</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-creating-and-managing-outbound-routing-rules">Visual Basic Example</a>