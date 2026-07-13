---
UID: NF:faxcom.IFaxServer.put_ServerCoverpage
title: IFaxServer::put_ServerCoverpage (faxcom.h)
description: Sets or retrieves the ServerCoverpage property for a FaxServer object. The ServerCoverpage property is a Boolean value that indicates whether the fax server permits the use of common cover pages only. (Put)
helpviewer_keywords: ["IFaxServer interface [Fax Service]","ServerCoverpage property","IFaxServer.ServerCoverpage","IFaxServer.get_ServerCoverpage","IFaxServer.put_ServerCoverpage","IFaxServer::ServerCoverpage","IFaxServer::get_ServerCoverpage","IFaxServer::put_ServerCoverpage","ServerCoverpage property [Fax Service]","ServerCoverpage property [Fax Service]","IFaxServer interface","_mfax_ifaxserver_get_servercoverpage","fax._mfax_ifaxserver_client_mfax_ifaxserver_get_servercoverpage_cpp","fax._mfax_ifaxserver_get_servercoverpage","faxcom/IFaxServer::ServerCoverpage","faxcom/IFaxServer::get_ServerCoverpage","faxcom/IFaxServer::put_ServerCoverpage","put_ServerCoverpage"]
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_servercoverpage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3gv9.htm
ms.date: 12/05/2018
ms.keywords: IFaxServer interface [Fax Service],ServerCoverpage property, IFaxServer.ServerCoverpage, IFaxServer.get_ServerCoverpage, IFaxServer.put_ServerCoverpage, IFaxServer::ServerCoverpage, IFaxServer::get_ServerCoverpage, IFaxServer::put_ServerCoverpage, ServerCoverpage property [Fax Service], ServerCoverpage property [Fax Service],IFaxServer interface, _mfax_ifaxserver_get_servercoverpage, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_servercoverpage_cpp, fax._mfax_ifaxserver_get_servercoverpage, faxcom/IFaxServer::ServerCoverpage, faxcom/IFaxServer::get_ServerCoverpage, faxcom/IFaxServer::put_ServerCoverpage, put_ServerCoverpage
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxServer::put_ServerCoverpage
 - faxcom/IFaxServer::put_ServerCoverpage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxServer.ServerCoverpage
 - IFaxServer.get_ServerCoverpage
 - IFaxServer.put_ServerCoverpage
 - IFaxServer.get_ServerCoverpage
 - IFaxServer.put_ServerCoverpage
---

# IFaxServer::put_ServerCoverpage


## -description

Sets or retrieves the <b>ServerCoverpage</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>ServerCoverpage</b> property is a Boolean value that indicates whether the fax server permits the use of common cover pages only. 

This property is read/write.

## -parameters

## -remarks

If you set the <b>ServerCoverpage</b> property equal to <b>TRUE</b>, users will be able to transmit only approved cover pages that are located on the fax server. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-cover-pages">Cover Pages</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-sending-a-cover-page">Sending a Cover Page</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-cover-pages">Cover Pages</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-sending-a-cover-page">Sending a Cover Page</a>
