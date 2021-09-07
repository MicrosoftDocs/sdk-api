---
UID: NF:faxcomex.IFaxOutboundRoutingRules.Add
title: IFaxOutboundRoutingRules::Add (faxcomex.h)
description: The IFaxOutboundRoutingRules::Add method adds an outbound routing rule (IFaxOutboundRoutingRule interface) to the collection defined by the IFaxOutboundRoutingRules interface.
helpviewer_keywords: ["Add","Add method [Fax Service]","Add method [Fax Service]","IFaxOutboundRoutingRules interface","IFaxOutboundRoutingRules interface [Fax Service]","Add method","IFaxOutboundRoutingRules.Add","IFaxOutboundRoutingRules::Add","_mfax_faxoutboundroutingrules.add_cpp","fax._mfax_faxoutboundroutingrules_add_cpp","faxcomex/IFaxOutboundRoutingRules::Add"]
old-location: fax\_mfax_faxoutboundroutingrules_add_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_50f8_cpp.htm
ms.date: 12/05/2018
ms.keywords: Add, Add method [Fax Service], Add method [Fax Service],IFaxOutboundRoutingRules interface, IFaxOutboundRoutingRules interface [Fax Service],Add method, IFaxOutboundRoutingRules.Add, IFaxOutboundRoutingRules::Add, _mfax_faxoutboundroutingrules.add_cpp, fax._mfax_faxoutboundroutingrules_add_cpp, faxcomex/IFaxOutboundRoutingRules::Add
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
 - IFaxOutboundRoutingRules::Add
 - faxcomex/IFaxOutboundRoutingRules::Add
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
 - IFaxOutboundRoutingRules.Add
---

# IFaxOutboundRoutingRules::Add


## -description

The <b>IFaxOutboundRoutingRules::Add</b> method adds an outbound routing rule (<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a> interface) to the collection defined by the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrules">IFaxOutboundRoutingRules</a> interface.

## -parameters

### -param lCountryCode

Type: <b>long</b>

A <b>long</b> value that specifies the country/region code to associate with the outbound routing rule. Specifying <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_routing_rule_code_enum">frrcANY_CODE</a> will add a rule that applies to any country/region code.

### -param lAreaCode

Type: <b>long</b>

Specifies a <b>long</b> value that indicates the area code to associate with the outbound routing rule. Specifying <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_routing_rule_code_enum">frrcANY_CODE</a> will add a rule that applies to any area code within the specified country/region code.

### -param bUseDevice

Type: <b>VARIANT_BOOL</b>

Specifies a Boolean value that indicates whether the outbound routing rule points to a single fax device rather than to a group of devices.

### -param bstrGroupName

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the name of the outbound routing group to which the new routing rule belongs. If <i>bUseDevice</i> is set to <b>TRUE</b>, this should be an empty string.

### -param lDeviceId

Type: <b>long</b>

Specifies the device to associate with the outbound routing rule. If <i>bUseDevice</i> is set to <b>FALSE</b>, this parameter is ignored.

### -param pFaxOutboundRoutingRule [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a>**</b>

An address of a pointer that receives a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method can also return remote procedure call (RPC) return values. For more information, see <a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.

To read or to write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrules">IFaxOutboundRoutingRules</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-creating-and-managing-outbound-routing-rules">Visual Basic Example</a>