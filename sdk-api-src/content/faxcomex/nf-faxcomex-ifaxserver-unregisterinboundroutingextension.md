---
UID: NF:faxcomex.IFaxServer.UnregisterInboundRoutingExtension
title: IFaxServer::UnregisterInboundRoutingExtension (faxcomex.h)
author: windows-sdk-content
description: The IFaxServer::UnregisterInboundRoutingExtension method unregisters an existing inbound routing extension. Unregistration will take place only after the fax server is restarted.
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_unregisterinboundroutingextension_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_2c32.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxServer interface [Fax Service],UnregisterInboundRoutingExtension method, IFaxServer.UnregisterInboundRoutingExtension, IFaxServer::UnregisterInboundRoutingExtension, UnregisterInboundRoutingExtension, UnregisterInboundRoutingExtension method [Fax Service], UnregisterInboundRoutingExtension method [Fax Service],IFaxServer interface, _mfax_faxserver.unregisterinboundroutingextension, fax._mfax_faxserver_cpp_mfax_faxserver_unregisterinboundroutingextension_cpp, fax._mfax_faxserver_unregisterinboundroutingextension, faxcomex/IFaxServer::UnregisterInboundRoutingExtension
ms.topic: method
f1_keywords: 
 - "faxcomex/IFaxServer.UnregisterInboundRoutingExtension"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxServer.UnregisterInboundRoutingExtension
 - IFaxServer.UnregisterInboundRoutingExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxServer::UnregisterInboundRoutingExtension


## -description


The <b>IFaxServer::UnregisterInboundRoutingExtension</b> method unregisters an existing inbound routing extension. Unregistration will take place only after the fax server is restarted.


## -parameters




### -param bstrExtensionUniqueName

TBD




#### - bstrExtensionName

Type: <b>BSTR</b>

String value that specifies the internal name of the fax routing extension DLL.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Only an administrator can unregister a routing extension. Also, this method works only on the local fax server.

To use this method, a user must have the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a>
 

 

