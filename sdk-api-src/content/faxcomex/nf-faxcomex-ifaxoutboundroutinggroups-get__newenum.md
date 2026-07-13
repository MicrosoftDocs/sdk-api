---
UID: NF:faxcomex.IFaxOutboundRoutingGroups.get__NewEnum
title: IFaxOutboundRoutingGroups::get__NewEnum (faxcomex.h)
description: The IFaxOutboundRoutingGroups::get__NewEnum method returns a reference to an enumerator object that you can use to iterate through the FaxOutboundRoutingGroups collection.
helpviewer_keywords: ["IFaxOutboundRoutingGroups interface [Fax Service]","get__NewEnum method","IFaxOutboundRoutingGroups.get__NewEnum","IFaxOutboundRoutingGroups::get__NewEnum","_mfax_ifaxoutboundroutinggroups_get__newenum","fax._mfax_ifaxoutboundroutinggroups_get__newenum","faxcomex/IFaxOutboundRoutingGroups::get__NewEnum","get__NewEnum","get__NewEnum method [Fax Service]","get__NewEnum method [Fax Service]","IFaxOutboundRoutingGroups interface"]
old-location: fax\_mfax_ifaxoutboundroutinggroups_get__newenum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0i7h.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutboundRoutingGroups interface [Fax Service],get__NewEnum method, IFaxOutboundRoutingGroups.get__NewEnum, IFaxOutboundRoutingGroups::get__NewEnum, _mfax_ifaxoutboundroutinggroups_get__newenum, fax._mfax_ifaxoutboundroutinggroups_get__newenum, faxcomex/IFaxOutboundRoutingGroups::get__NewEnum, get__NewEnum, get__NewEnum method [Fax Service], get__NewEnum method [Fax Service],IFaxOutboundRoutingGroups interface
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
 - IFaxOutboundRoutingGroups::get__NewEnum
 - faxcomex/IFaxOutboundRoutingGroups::get__NewEnum
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
 - IFaxOutboundRoutingGroups.get__NewEnum
---

# IFaxOutboundRoutingGroups::get__NewEnum


## -description

The <b>IFaxOutboundRoutingGroups::get__NewEnum</b> method returns a reference to an enumerator object that you can use to iterate through the <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutinggroups">FaxOutboundRoutingGroups</a> collection.

## -parameters

### -param ppUnk [out, retval]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

Receives an indirect pointer to the enumerator object's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface for this collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutinggroups">IFaxOutboundRoutingGroups</a>