---
UID: NF:faxcomex.IFaxInboundRoutingMethod.Refresh
title: IFaxInboundRoutingMethod::Refresh (faxcomex.h)
description: The IFaxInboundRoutingMethod::Refresh method refreshes IFaxInboundRoutingMethod interface information from the fax server.
helpviewer_keywords: ["IFaxInboundRoutingMethod interface [Fax Service]","Refresh method","IFaxInboundRoutingMethod.Refresh","IFaxInboundRoutingMethod::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxInboundRoutingMethod interface","_mfax_faxinboundroutingmethod.refresh","fax._mfax_faxinboundroutingmethod_cpp_mfax_faxinboundroutingmethod_refresh_cpp","fax._mfax_faxinboundroutingmethod_refresh","faxcomex/IFaxInboundRoutingMethod::Refresh"]
old-location: fax\_mfax_faxinboundroutingmethod_cpp_mfax_faxinboundroutingmethod_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_42aw.htm
ms.date: 12/05/2018
ms.keywords: IFaxInboundRoutingMethod interface [Fax Service],Refresh method, IFaxInboundRoutingMethod.Refresh, IFaxInboundRoutingMethod::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxInboundRoutingMethod interface, _mfax_faxinboundroutingmethod.refresh, fax._mfax_faxinboundroutingmethod_cpp_mfax_faxinboundroutingmethod_refresh_cpp, fax._mfax_faxinboundroutingmethod_refresh, faxcomex/IFaxInboundRoutingMethod::Refresh
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
 - IFaxInboundRoutingMethod::Refresh
 - faxcomex/IFaxInboundRoutingMethod::Refresh
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
 - IFaxInboundRoutingMethod.Refresh
 - IFaxInboundRoutingMethod.Refresh
---

# IFaxInboundRoutingMethod::Refresh


## -description

The <b>IFaxInboundRoutingMethod::Refresh</b> method refreshes <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingmethod">IFaxInboundRoutingMethod</a> interface information from the fax server.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the <b>IFaxInboundRoutingMethod::Refresh</b> method is called, any configuration changes made after the last <a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod-save-vb">IFaxInboundRoutingMethod::Save</a> method call are lost.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxinboundroutingmethod">FaxInboundRoutingMethod</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundroutingmethod">IFaxInboundRoutingMethod</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-routing-extensions-and-routing-methods">Visual Basic Example</a>
