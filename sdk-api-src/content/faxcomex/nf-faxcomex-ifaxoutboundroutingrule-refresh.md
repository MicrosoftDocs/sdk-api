---
UID: NF:faxcomex.IFaxOutboundRoutingRule.Refresh
title: IFaxOutboundRoutingRule::Refresh (faxcomex.h)
description: The IFaxOutboundRoutingRule::Refresh method refreshes FaxOutboundRoutingRule object information from the fax server.
helpviewer_keywords: ["IFaxOutboundRoutingRule interface [Fax Service]","Refresh method","IFaxOutboundRoutingRule.Refresh","IFaxOutboundRoutingRule::Refresh","Refresh","Refresh method [Fax Service]","Refresh method [Fax Service]","IFaxOutboundRoutingRule interface","_mfax_faxoutboundroutingrule.refresh","fax._mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_refresh_cpp","fax._mfax_faxoutboundroutingrule_refresh","faxcomex/IFaxOutboundRoutingRule::Refresh"]
old-location: fax\_mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6s2w.htm
ms.date: 12/05/2018
ms.keywords: IFaxOutboundRoutingRule interface [Fax Service],Refresh method, IFaxOutboundRoutingRule.Refresh, IFaxOutboundRoutingRule::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxOutboundRoutingRule interface, _mfax_faxoutboundroutingrule.refresh, fax._mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_refresh_cpp, fax._mfax_faxoutboundroutingrule_refresh, faxcomex/IFaxOutboundRoutingRule::Refresh
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
 - IFaxOutboundRoutingRule::Refresh
 - faxcomex/IFaxOutboundRoutingRule::Refresh
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
 - IFaxOutboundRoutingRule.Refresh
 - IFaxOutboundRoutingRule.Refresh
---

# IFaxOutboundRoutingRule::Refresh


## -description

The <b>IFaxOutboundRoutingRule::Refresh</b> method refreshes <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule">FaxOutboundRoutingRule</a> object information from the fax server.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the <b>IFaxOutboundRoutingRule::Refresh</b> method is called, any configuration changes made after the last <a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule-save-vb">IFaxOutboundRoutingRule::Save</a> method call are lost.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxoutboundroutingrule">FaxOutboundRoutingRule</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrule">IFaxOutboundRoutingRule</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-creating-and-managing-outbound-routing-rules">Visual Basic Example</a>
