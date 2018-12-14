---
UID: NF:faxcom.IFaxServer.Connect
title: IFaxServer::Connect
author: windows-sdk-content
description: The Connect method connects a fax client application to the specified fax server.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_connect_client_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7984.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Connect, Connect method [Fax Service], Connect method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],Connect method, IFaxServer.Connect, IFaxServer::Connect, _mfax_ifaxserver_connect_client, fax._mfax_ifaxserver_client_mfax_ifaxserver_connect_client_cpp, fax._mfax_ifaxserver_connect_client, faxcom/IFaxServer::Connect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxServer::Connect


## -description


The <b>Connect</b> method connects a fax client application to the specified fax server. Before accessing most interfaces that begin with <b>IFax</b>, the application must call this method to initiate a connection with an active fax server. A fax server connection is not required to access an <a href="https://msdn.microsoft.com/a4c46893-502d-4d5c-a895-837cffc014e4">IFaxTiff</a> interface.


## -parameters




### -param ServerName [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the name of the target fax server. If this parameter is <b>NULL</b>, the method connects the application to the fax server on the local computer. See <a href="https://msdn.microsoft.com/da213475-2cfb-4524-80af-51c1ee0bf658">Connecting to a Fax Server</a> for limitations on connecting to remote servers.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The fax client application must call the <a href="https://msdn.microsoft.com/dccbb6b1-b889-4b73-a3d0-9c5ce6268f4a">IFaxServer::Disconnect</a> method to disconnect from the fax server.

For more information, see <a href="https://msdn.microsoft.com/da213475-2cfb-4524-80af-51c1ee0bf658">Connecting to a Fax Server</a> and <a href="https://msdn.microsoft.com/02d276b7-bcbc-4bbe-8051-d9b35f12dc93">Disconnecting from a Fax Server</a>.




## -see-also




<a href="https://msdn.microsoft.com/da213475-2cfb-4524-80af-51c1ee0bf658">Connecting to a Fax Server</a>



<a href="https://msdn.microsoft.com/02d276b7-bcbc-4bbe-8051-d9b35f12dc93">Disconnecting from a Fax Server</a>



<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a>



<a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a>



<a href="https://msdn.microsoft.com/dccbb6b1-b889-4b73-a3d0-9c5ce6268f4a">IFaxServer::Disconnect</a>
 

 

