---
UID: NF:faxcom.IFaxServer.Connect
title: IFaxServer::Connect (faxcom.h)
description: The Connect method connects a fax client application to the specified fax server.
helpviewer_keywords: ["Connect","Connect method [Fax Service]","Connect method [Fax Service]","IFaxServer interface","IFaxServer interface [Fax Service]","Connect method","IFaxServer.Connect","IFaxServer::Connect","_mfax_ifaxserver_connect_client","fax._mfax_ifaxserver_client_mfax_ifaxserver_connect_client_cpp","fax._mfax_ifaxserver_connect_client","faxcom/IFaxServer::Connect"]
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_connect_client_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7984.htm
ms.date: 12/05/2018
ms.keywords: Connect, Connect method [Fax Service], Connect method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],Connect method, IFaxServer.Connect, IFaxServer::Connect, _mfax_ifaxserver_connect_client, fax._mfax_ifaxserver_client_mfax_ifaxserver_connect_client_cpp, fax._mfax_ifaxserver_connect_client, faxcom/IFaxServer::Connect
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
 - IFaxServer::Connect
 - faxcom/IFaxServer::Connect
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
 - IFaxServer.Connect
 - IFaxServer.Connect
---

# IFaxServer::Connect


## -description

The <b>Connect</b> method connects a fax client application to the specified fax server. Before accessing most interfaces that begin with <b>IFax</b>, the application must call this method to initiate a connection with an active fax server. A fax server connection is not required to access an <a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxtiff">IFaxTiff</a> interface.

## -parameters

### -param ServerName [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the name of the target fax server. If this parameter is <b>NULL</b>, the method connects the application to the fax server on the local computer. See <a href="/previous-versions/windows/desktop/fax/-mfax-connecting-to-a-fax-server">Connecting to a Fax Server</a> for limitations on connecting to remote servers.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The fax client application must call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-disconnect-client-vb">IFaxServer::Disconnect</a> method to disconnect from the fax server.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-connecting-to-a-fax-server">Connecting to a Fax Server</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-disconnecting-from-a-fax-server">Disconnecting from a Fax Server</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-connecting-to-a-fax-server">Connecting to a Fax Server</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-disconnecting-from-a-fax-server">Disconnecting from a Fax Server</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-ifaxserver-disconnect-client-vb">IFaxServer::Disconnect</a>