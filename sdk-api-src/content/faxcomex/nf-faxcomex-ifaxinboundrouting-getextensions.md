---
UID: NF:faxcomex.IFaxInboundRouting.GetExtensions
title: IFaxInboundRouting::GetExtensions (faxcomex.h)
description: The GetExtensions method retrieves the collection of inbound routing extensions registered with the fax service.
helpviewer_keywords: ["GetExtensions","GetExtensions method [Fax Service]","GetExtensions method [Fax Service]","IFaxInboundRouting interface","IFaxInboundRouting interface [Fax Service]","GetExtensions method","IFaxInboundRouting.GetExtensions","IFaxInboundRouting::GetExtensions","_mfax_faxinboundrouting.getextensions_cpp","fax._mfax_faxinboundrouting_getextensions_cpp","faxcomex/IFaxInboundRouting::GetExtensions"]
old-location: fax\_mfax_faxinboundrouting_getextensions_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_80oj_cpp.htm
ms.date: 12/05/2018
ms.keywords: GetExtensions, GetExtensions method [Fax Service], GetExtensions method [Fax Service],IFaxInboundRouting interface, IFaxInboundRouting interface [Fax Service],GetExtensions method, IFaxInboundRouting.GetExtensions, IFaxInboundRouting::GetExtensions, _mfax_faxinboundrouting.getextensions_cpp, fax._mfax_faxinboundrouting_getextensions_cpp, faxcomex/IFaxInboundRouting::GetExtensions
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
 - IFaxInboundRouting::GetExtensions
 - faxcomex/IFaxInboundRouting::GetExtensions
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
 - IFaxInboundRouting.GetExtensions
---

# IFaxInboundRouting::GetExtensions


## -description

The <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundrouting-getextensions">GetExtensions</a> method retrieves the collection of inbound routing extensions registered with the fax service.

## -parameters

### -param pFaxInboundRoutingExtensions [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingextensions">IFaxInboundRoutingExtensions</a>**</b>

Address of a pointer to an <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingextensions">IFaxInboundRoutingExtensions</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundrouting">IFaxInboundRouting</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-routing-extensions-and-routing-methods">Visual Basic Example</a>