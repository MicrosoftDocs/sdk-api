---
UID: NF:faxcom.IFaxServer.Disconnect
title: IFaxServer::Disconnect
author: windows-sdk-content
description: The IFaxServer::Disconnect method terminates a fax client application's connection to a fax server.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_disconnect_client_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5w50.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Disconnect, Disconnect method [Fax Service], Disconnect method [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],Disconnect method, IFaxServer.Disconnect, IFaxServer::Disconnect, _mfax_ifaxserver_disconnect_client, fax._mfax_ifaxserver_client_mfax_ifaxserver_disconnect_client_cpp, fax._mfax_ifaxserver_disconnect_client, faxcom/IFaxServer::Disconnect
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
 - IFaxServer.Disconnect
 - IFaxServer.Disconnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxServer::Disconnect


## -description


The <b>IFaxServer::Disconnect</b> method terminates a fax client application's connection to a fax server.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A call to the <b>IFaxServer::Disconnect</b> method attempts to terminate a server connection made by a previous call to the <a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">IFaxServer::Connect</a> method.

In addition to calling the <b>IFaxServer::Disconnect</b> method, an application must also call the <a href="_com_IUnknown_Release">IUnknown::Release</a> method to allow each object to deallocate itself.

For more information, see <a href="https://msdn.microsoft.com/da213475-2cfb-4524-80af-51c1ee0bf658">Connecting to a Fax Server</a> and <a href="https://msdn.microsoft.com/02d276b7-bcbc-4bbe-8051-d9b35f12dc93">Disconnecting from a Fax Server</a>.




## -see-also




<a href="https://msdn.microsoft.com/da213475-2cfb-4524-80af-51c1ee0bf658">Connecting to a Fax Server</a>



<a href="https://msdn.microsoft.com/02d276b7-bcbc-4bbe-8051-d9b35f12dc93">Disconnecting from a Fax Server</a>



<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a>



<a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a>



<a href="https://msdn.microsoft.com/12e71c4c-c4b5-4e6d-a1fa-b833d6a00ff8">IFaxServer::Connect</a>



<a href="_com_IUnknown_Release">IUnknown::Release</a>
 

 

