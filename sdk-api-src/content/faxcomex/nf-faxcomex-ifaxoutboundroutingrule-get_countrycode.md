---
UID: NF:faxcomex.IFaxOutboundRoutingRule.get_CountryCode
title: IFaxOutboundRoutingRule::get_CountryCode (faxcomex.h)
description: The IFaxOutboundRoutingRule::get_CountryCode property specifies the country/region code to which the outbound routing rule applies.
helpviewer_keywords: ["CountryCode property [Fax Service]","CountryCode property [Fax Service]","IFaxOutboundRoutingRule interface","IFaxOutboundRoutingRule interface [Fax Service]","CountryCode property","IFaxOutboundRoutingRule.CountryCode","IFaxOutboundRoutingRule.get_CountryCode","IFaxOutboundRoutingRule::CountryCode","IFaxOutboundRoutingRule::get_CountryCode","_mfax_faxoutboundroutingrule.countrycode","fax._mfax_faxoutboundroutingrule_countrycode","fax._mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_countrycode_cpp","faxcomex/IFaxOutboundRoutingRule::CountryCode","faxcomex/IFaxOutboundRoutingRule::get_CountryCode","get_CountryCode"]
old-location: fax\_mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_countrycode_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5ysl.htm
ms.date: 12/05/2018
ms.keywords: CountryCode property [Fax Service], CountryCode property [Fax Service],IFaxOutboundRoutingRule interface, IFaxOutboundRoutingRule interface [Fax Service],CountryCode property, IFaxOutboundRoutingRule.CountryCode, IFaxOutboundRoutingRule.get_CountryCode, IFaxOutboundRoutingRule::CountryCode, IFaxOutboundRoutingRule::get_CountryCode, _mfax_faxoutboundroutingrule.countrycode, fax._mfax_faxoutboundroutingrule_countrycode, fax._mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_countrycode_cpp, faxcomex/IFaxOutboundRoutingRule::CountryCode, faxcomex/IFaxOutboundRoutingRule::get_CountryCode, get_CountryCode
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
 - IFaxOutboundRoutingRule::get_CountryCode
 - faxcomex/IFaxOutboundRoutingRule::get_CountryCode
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
 - IFaxOutboundRoutingRule.CountryCode
 - IFaxOutboundRoutingRule.get_CountryCode
---

# IFaxOutboundRoutingRule::get_CountryCode


## -description

The <b>IFaxOutboundRoutingRule::get_CountryCode</b> property specifies the country/region code to which the outbound routing rule applies.

This property is read-only.

## -parameters

## -remarks

If this property is equal to <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_routing_rule_code_enum">frrcANY_CODE</a>, the outbound routing rule applies to all country/region codes.

To read this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule">FaxOutboundRoutingRule</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-creating-and-managing-outbound-routing-rules">Visual Basic Example</a>