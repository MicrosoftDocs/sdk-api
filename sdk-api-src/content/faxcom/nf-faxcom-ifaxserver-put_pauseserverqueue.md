---
UID: NF:faxcom.IFaxServer.put_PauseServerQueue
title: IFaxServer::put_PauseServerQueue (faxcom.h)
description: Sets or retrieves the PauseServerQueue property for a FaxServer object. The PauseServerQueue property is a Boolean value that indicates whether the fax server has paused the fax job queue. (Put)
helpviewer_keywords: ["IFaxServer interface [Fax Service]","PauseServerQueue property","IFaxServer.PauseServerQueue","IFaxServer.get_PauseServerQueue","IFaxServer.put_PauseServerQueue","IFaxServer::PauseServerQueue","IFaxServer::get_PauseServerQueue","IFaxServer::put_PauseServerQueue","PauseServerQueue property [Fax Service]","PauseServerQueue property [Fax Service]","IFaxServer interface","_mfax_ifaxserver_get_pauseserverqueue","fax._mfax_ifaxserver_client_mfax_ifaxserver_get_pauseserverqueue_cpp","fax._mfax_ifaxserver_get_pauseserverqueue","faxcom/IFaxServer::PauseServerQueue","faxcom/IFaxServer::get_PauseServerQueue","faxcom/IFaxServer::put_PauseServerQueue","put_PauseServerQueue"]
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_pauseserverqueue_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9gv9.htm
ms.date: 12/05/2018
ms.keywords: IFaxServer interface [Fax Service],PauseServerQueue property, IFaxServer.PauseServerQueue, IFaxServer.get_PauseServerQueue, IFaxServer.put_PauseServerQueue, IFaxServer::PauseServerQueue, IFaxServer::get_PauseServerQueue, IFaxServer::put_PauseServerQueue, PauseServerQueue property [Fax Service], PauseServerQueue property [Fax Service],IFaxServer interface, _mfax_ifaxserver_get_pauseserverqueue, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_pauseserverqueue_cpp, fax._mfax_ifaxserver_get_pauseserverqueue, faxcom/IFaxServer::PauseServerQueue, faxcom/IFaxServer::get_PauseServerQueue, faxcom/IFaxServer::put_PauseServerQueue, put_PauseServerQueue
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
 - IFaxServer::put_PauseServerQueue
 - faxcom/IFaxServer::put_PauseServerQueue
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
 - IFaxServer.PauseServerQueue
 - IFaxServer.get_PauseServerQueue
 - IFaxServer.put_PauseServerQueue
 - IFaxServer.get_PauseServerQueue
 - IFaxServer.put_PauseServerQueue
---

# IFaxServer::put_PauseServerQueue


## -description

Sets or retrieves the <b>PauseServerQueue</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>PauseServerQueue</b> property is a Boolean value that indicates whether the fax server has paused the fax job queue.

This property is read/write.

## -parameters

## -remarks

An administrator might pause the fax job queue for various reasons. For example, the administrator may need to perform queue management, or free a fax device for an inbound reception or for another application's use.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a>
