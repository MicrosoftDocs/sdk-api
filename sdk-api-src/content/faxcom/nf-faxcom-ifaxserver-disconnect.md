---
UID: NF:faxcom.IFaxServer.Disconnect
title: IFaxServer::Disconnect (faxcom.h)
author: windows-sdk-content
description: The IFaxServer::Disconnect method terminates a fax client application's connection to a fax server.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_disconnect_client_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5w50.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
---

# IFaxServer::Disconnect


## -description


The <b>IFaxServer::Disconnect</b> method terminates a fax client application's connection to a fax server.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A call to the <b>IFaxServer::Disconnect</b> method attempts to terminate a server connection made by a previous call to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">IFaxServer::Connect</a> method.

In addition to calling the <b>IFaxServer::Disconnect</b> method, an application must also call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method to allow each object to deallocate itself.

For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-connecting-to-a-fax-server">Connecting to a Fax Server</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-disconnecting-from-a-fax-server">Disconnecting from a Fax Server</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-connecting-to-a-fax-server">Connecting to a Fax Server</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-disconnecting-from-a-fax-server">Disconnecting from a Fax Server</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-ifaxserver-connect-client-vb">IFaxServer::Connect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>
 

 

