---
UID: NF:faxcomex.IFaxOutboundRoutingRules.get_Item
title: IFaxOutboundRoutingRules::get_Item (faxcomex.h)
description: The IFaxOutboundRoutingRules::get_Item method returns a IFaxOutboundRoutingRule interface from the IFaxOutboundRoutingRules interface using the routing rule's index.
helpviewer_keywords: ["IFaxOutboundRoutingRules interface [Fax Service]","get_Item method","IFaxOutboundRoutingRules.get_Item","IFaxOutboundRoutingRules::get_Item","_mfax_faxoutboundroutingrules.item_cpp","fax._mfax_faxoutboundroutingrules_item_cpp","faxcomex/IFaxOutboundRoutingRules::get_Item","get_Item","get_Item method [Fax Service]","get_Item method [Fax Service]","IFaxOutboundRoutingRules interface"]
old-location: fax\_mfax_faxoutboundroutingrules_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_73xp_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutboundRoutingRules interface [Fax Service],get_Item method, IFaxOutboundRoutingRules.get_Item, IFaxOutboundRoutingRules::get_Item, _mfax_faxoutboundroutingrules.item_cpp, fax._mfax_faxoutboundroutingrules_item_cpp, faxcomex/IFaxOutboundRoutingRules::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxOutboundRoutingRules interface
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
 - IFaxOutboundRoutingRules::get_Item
 - faxcomex/IFaxOutboundRoutingRules::get_Item
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
 - IFaxOutboundRoutingRules.get_Item
---

# IFaxOutboundRoutingRules::get_Item


## -description

The <b>IFaxOutboundRoutingRules::get_Item</b> method returns a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a> interface from the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrules">IFaxOutboundRoutingRules</a> interface using the routing rule's index.

## -parameters

### -param lIndex [in]

Type: <b>long</b>

A <b>long</b> value that specifies the outbound routing rule to retrieve from the collection. Valid values for this parameter are in the range from 1 to n, where n is the number of items returned by a call to the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrules-count-vb">IFaxOutboundRoutingRules::get_Count</a> method.

### -param pFaxOutboundRoutingRule [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a>**</b>

An address of a pointer that receives the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrules">IFaxOutboundRoutingRules</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-creating-and-managing-outbound-routing-rules">Visual Basic Example</a>