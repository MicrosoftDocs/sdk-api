---
UID: NF:faxcomex.IFaxOutboundRoutingRule.get_AreaCode
title: IFaxOutboundRoutingRule::get_AreaCode (faxcomex.h)
description: The IFaxOutboundRoutingRule::get_AreaCode property specifies the area code to which the outbound routing rule applies.
helpviewer_keywords: ["AreaCode property [Fax Service]","AreaCode property [Fax Service]","IFaxOutboundRoutingRule interface","IFaxOutboundRoutingRule interface [Fax Service]","AreaCode property","IFaxOutboundRoutingRule.AreaCode","IFaxOutboundRoutingRule.get_AreaCode","IFaxOutboundRoutingRule::AreaCode","IFaxOutboundRoutingRule::get_AreaCode","_mfax_faxoutboundroutingrule.areacode","fax._mfax_faxoutboundroutingrule_areacode","fax._mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_areacode_cpp","faxcomex/IFaxOutboundRoutingRule::AreaCode","faxcomex/IFaxOutboundRoutingRule::get_AreaCode","get_AreaCode"]
old-location: fax\_mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_areacode_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_1git.htm
ms.date: 12/05/2018
ms.keywords: AreaCode property [Fax Service], AreaCode property [Fax Service],IFaxOutboundRoutingRule interface, IFaxOutboundRoutingRule interface [Fax Service],AreaCode property, IFaxOutboundRoutingRule.AreaCode, IFaxOutboundRoutingRule.get_AreaCode, IFaxOutboundRoutingRule::AreaCode, IFaxOutboundRoutingRule::get_AreaCode, _mfax_faxoutboundroutingrule.areacode, fax._mfax_faxoutboundroutingrule_areacode, fax._mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_areacode_cpp, faxcomex/IFaxOutboundRoutingRule::AreaCode, faxcomex/IFaxOutboundRoutingRule::get_AreaCode, get_AreaCode
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
 - IFaxOutboundRoutingRule::get_AreaCode
 - faxcomex/IFaxOutboundRoutingRule::get_AreaCode
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
 - IFaxOutboundRoutingRule.AreaCode
 - IFaxOutboundRoutingRule.get_AreaCode
---

# IFaxOutboundRoutingRule::get_AreaCode


## -description

The <b>IFaxOutboundRoutingRule::get_AreaCode</b> property specifies the area code to which the outbound routing rule applies.

This property is read-only.

## -parameters

## -remarks

If this property is equal to <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_routing_rule_code_enum">frrcANY_CODE</a>, the outbound routing rule applies to all area codes.

To read this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule">FaxOutboundRoutingRule</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-creating-and-managing-outbound-routing-rules">Visual Basic Example</a>