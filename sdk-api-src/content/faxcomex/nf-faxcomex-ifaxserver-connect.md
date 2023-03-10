---
UID: NF:faxcomex.IFaxServer.Connect
title: IFaxServer::Connect (faxcomex.h)
description: The IFaxServer::Connect method connects a fax client application to the specified fax server.
helpviewer_keywords: ["Connect","Connect method [Fax Service]","Connect method [Fax Service]","IFaxServer interface","IFaxServer interface [Fax Service]","Connect method","IFaxServer.Connect","IFaxServer::Connect","_mfax_faxserver.connect","fax._mfax_faxserver_connect","fax._mfax_faxserver_cpp_mfax_faxserver_connect_cpp","faxcomex/IFaxServer::Connect"]
old-location: fax\_mfax_faxserver_cpp_mfax_faxserver_connect_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_0ipg.htm
ms.date: 12/05/2018
ms.keywords: Connect, Connect method [Fax Service], Connect method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],Connect method, IFaxServer.Connect, IFaxServer::Connect, _mfax_faxserver.connect, fax._mfax_faxserver_connect, fax._mfax_faxserver_cpp_mfax_faxserver_connect_cpp, faxcomex/IFaxServer::Connect
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
 - IFaxServer::Connect
 - faxcomex/IFaxServer::Connect
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
 - IFaxServer.Connect
---

# IFaxServer::Connect


## -description

The <b>IFaxServer::Connect</b> method connects a fax client application to the specified fax server.

## -parameters

### -param bstrServerName

Type: <b>BSTR</b>

A null-terminated string that specifies the name of the target fax server, such as "computername". If this parameter is <b>NULL</b> or an empty string, the method connects the application to the fax server on the local computer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Before accessing most of the objects of the fax extended Component Object Model (COM), the application must call this method to initiate a connection with an active fax server. A fax server connection is not required for you to access a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdocument">FaxDocument</a> object. The method fails if the client is not connected to an active fax server. 

To connect to the local server, set the <i>bstrServerName</i> parameter to <b>NULL</b> or an empty string. For usage examples, see <a href="/previous-versions/windows/desktop/fax/-mfax-connecting-to-the-fax-server">Connecting to the Fax Server</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver">IFaxServer</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-retrieving-server-properties">Visual Basic Example</a>