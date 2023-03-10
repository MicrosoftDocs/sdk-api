---
UID: NF:faxcomex.IFaxServer.get_OutboundRouting
title: IFaxServer::get_OutboundRouting (faxcomex.h)
description: The IFaxServer::get_OutboundRouting property creates a IFaxOutboundRouting configuration interface. The interface permits users to configure outbound routing groups and rules.
helpviewer_keywords: ["IFaxServer interface [Fax Service]","OutboundRouting property","IFaxServer.OutboundRouting","IFaxServer.get_OutboundRouting","IFaxServer::OutboundRouting","IFaxServer::get_OutboundRouting","OutboundRouting property [Fax Service]","OutboundRouting property [Fax Service]","IFaxServer interface","_mfax_faxserver.outboundrouting_cpp","fax._mfax_faxserver_outboundrouting_cpp","faxcomex/IFaxServer::OutboundRouting","faxcomex/IFaxServer::get_OutboundRouting","get_OutboundRouting"]
old-location: fax\_mfax_faxserver_outboundrouting_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6y1z_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxServer interface [Fax Service],OutboundRouting property, IFaxServer.OutboundRouting, IFaxServer.get_OutboundRouting, IFaxServer::OutboundRouting, IFaxServer::get_OutboundRouting, OutboundRouting property [Fax Service], OutboundRouting property [Fax Service],IFaxServer interface, _mfax_faxserver.outboundrouting_cpp, fax._mfax_faxserver_outboundrouting_cpp, faxcomex/IFaxServer::OutboundRouting, faxcomex/IFaxServer::get_OutboundRouting, get_OutboundRouting
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
 - IFaxServer::get_OutboundRouting
 - faxcomex/IFaxServer::get_OutboundRouting
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
 - IFaxServer.OutboundRouting
 - IFaxServer.get_OutboundRouting
---

# IFaxServer::get_OutboundRouting


## -description

The <b>IFaxServer::get_OutboundRouting</b> property creates a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundrouting">IFaxOutboundRouting</a> configuration interface. The interface permits users to configure outbound routing groups and rules.

This property is read-only.

## -parameters

## -remarks

This property is not supported in Windows XP, and will return the error: <a href="/previous-versions/windows/desktop/fax/-mfax-fax-error-codes">FAX_E_NOT_SUPPORTED_ON_THIS_SKU</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outbound-routing-groups">Visual Basic Example</a>