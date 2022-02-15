---
UID: NF:faxcomex.IFaxInboundRouting.GetMethods
title: IFaxInboundRouting::GetMethods (faxcomex.h)
description: The IFaxInboundRouting::GetMethods method retrieves the ordered collection of all the inbound routing methods exposed by all the inbound routing extensions currently registered with the fax service.
helpviewer_keywords: ["GetMethods","GetMethods method [Fax Service]","GetMethods method [Fax Service]","IFaxInboundRouting interface","IFaxInboundRouting interface [Fax Service]","GetMethods method","IFaxInboundRouting.GetMethods","IFaxInboundRouting::GetMethods","_mfax_faxinboundrouting.getmethods_cpp","fax._mfax_faxinboundrouting_getmethods_cpp","faxcomex/IFaxInboundRouting::GetMethods"]
old-location: fax\_mfax_faxinboundrouting_getmethods_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_2x9v_cpp.htm
ms.date: 12/05/2018
ms.keywords: GetMethods, GetMethods method [Fax Service], GetMethods method [Fax Service],IFaxInboundRouting interface, IFaxInboundRouting interface [Fax Service],GetMethods method, IFaxInboundRouting.GetMethods, IFaxInboundRouting::GetMethods, _mfax_faxinboundrouting.getmethods_cpp, fax._mfax_faxinboundrouting_getmethods_cpp, faxcomex/IFaxInboundRouting::GetMethods
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
 - IFaxInboundRouting::GetMethods
 - faxcomex/IFaxInboundRouting::GetMethods
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
 - IFaxInboundRouting.GetMethods
---

# IFaxInboundRouting::GetMethods


## -description

The <b>IFaxInboundRouting::GetMethods</b> method retrieves the ordered collection of all the inbound routing methods exposed by all the inbound routing extensions currently registered with the fax service.

## -parameters

### -param pFaxInboundRoutingMethods [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingmethods">IFaxInboundRoutingMethods</a>**</b>

Address of a pointer to an <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingmethods">IFaxInboundRoutingMethods</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Order is based on the <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-priority">Priority</a> property of each routing method. The priority is associated with the order in which the fax service calls the routing method when the service receives a fax job.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundrouting">IFaxInboundRouting</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-routing-extensions-and-routing-methods">Visual Basic Example</a>