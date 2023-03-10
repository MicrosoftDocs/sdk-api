---
UID: NF:faxcom.IFaxServer.put_Retries
title: IFaxServer::put_Retries (faxcom.h)
description: Sets or retrieves the Retries property for a FaxServer object. The Retries property is a value that represents the number of times the fax server attempts to retransmit an outgoing fax when the initial transmission fails. (Put)
helpviewer_keywords: ["IFaxServer interface [Fax Service]","Retries property","IFaxServer.Retries","IFaxServer.get_Retries","IFaxServer.put_Retries","IFaxServer::Retries","IFaxServer::get_Retries","IFaxServer::put_Retries","Retries property [Fax Service]","Retries property [Fax Service]","IFaxServer interface","_mfax_ifaxserver_get_retries","fax._mfax_ifaxserver_client_mfax_ifaxserver_get_retries_cpp","fax._mfax_ifaxserver_get_retries","faxcom/IFaxServer::Retries","faxcom/IFaxServer::get_Retries","faxcom/IFaxServer::put_Retries","put_Retries"]
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_retries_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3veb.htm
ms.date: 12/05/2018
ms.keywords: IFaxServer interface [Fax Service],Retries property, IFaxServer.Retries, IFaxServer.get_Retries, IFaxServer.put_Retries, IFaxServer::Retries, IFaxServer::get_Retries, IFaxServer::put_Retries, Retries property [Fax Service], Retries property [Fax Service],IFaxServer interface, _mfax_ifaxserver_get_retries, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_retries_cpp, fax._mfax_ifaxserver_get_retries, faxcom/IFaxServer::Retries, faxcom/IFaxServer::get_Retries, faxcom/IFaxServer::put_Retries, put_Retries
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
 - IFaxServer::put_Retries
 - faxcom/IFaxServer::put_Retries
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
 - IFaxServer.Retries
 - IFaxServer.get_Retries
 - IFaxServer.put_Retries
 - IFaxServer.get_Retries
 - IFaxServer.put_Retries
---

# IFaxServer::put_Retries


## -description

Sets or retrieves the <b>Retries</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>Retries</b> property is a value that represents the number of times the fax server attempts to retransmit an outgoing fax when the initial transmission fails.

This property is read/write.

## -parameters

## -remarks

A transmission might not be sent on the first attempt for various reasons. For example, the sending device may receive a busy signal.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a>
