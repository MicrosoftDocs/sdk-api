---
UID: NF:faxcom.IFaxServer.put_RetryDelay
title: IFaxServer::put_RetryDelay (faxcom.h)
description: Sets or retrieves the RetryDelay property for a FaxServer object. The RetryDelay property is a value that represents the time interval, in minutes, the fax server waits before attempting to retransmit an outbound fax job. (Put)
helpviewer_keywords: ["IFaxServer interface [Fax Service]","RetryDelay property","IFaxServer.RetryDelay","IFaxServer.get_RetryDelay","IFaxServer.put_RetryDelay","IFaxServer::RetryDelay","IFaxServer::get_RetryDelay","IFaxServer::put_RetryDelay","RetryDelay property [Fax Service]","RetryDelay property [Fax Service]","IFaxServer interface","_mfax_ifaxserver_get_retrydelay","fax._mfax_ifaxserver_client_mfax_ifaxserver_get_retrydelay_cpp","fax._mfax_ifaxserver_get_retrydelay","faxcom/IFaxServer::RetryDelay","faxcom/IFaxServer::get_RetryDelay","faxcom/IFaxServer::put_RetryDelay","put_RetryDelay"]
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_retrydelay_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6at5.htm
ms.date: 12/05/2018
ms.keywords: IFaxServer interface [Fax Service],RetryDelay property, IFaxServer.RetryDelay, IFaxServer.get_RetryDelay, IFaxServer.put_RetryDelay, IFaxServer::RetryDelay, IFaxServer::get_RetryDelay, IFaxServer::put_RetryDelay, RetryDelay property [Fax Service], RetryDelay property [Fax Service],IFaxServer interface, _mfax_ifaxserver_get_retrydelay, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_retrydelay_cpp, fax._mfax_ifaxserver_get_retrydelay, faxcom/IFaxServer::RetryDelay, faxcom/IFaxServer::get_RetryDelay, faxcom/IFaxServer::put_RetryDelay, put_RetryDelay
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
 - IFaxServer::put_RetryDelay
 - faxcom/IFaxServer::put_RetryDelay
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
 - IFaxServer.RetryDelay
 - IFaxServer.get_RetryDelay
 - IFaxServer.put_RetryDelay
 - IFaxServer.get_RetryDelay
 - IFaxServer.put_RetryDelay
---

# IFaxServer::put_RetryDelay


## -description

Sets or retrieves the <b>RetryDelay</b> property for a <a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a> object. The <b>RetryDelay</b> property is a value that represents the time interval, in minutes, the fax server waits before attempting to retransmit an outbound fax job.

This property is read/write.

## -parameters

## -remarks

A transmission might not be sent on the first attempt for various reasons. For example, the sending device may receive a busy signal.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-faxserver-client">FaxServer</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxserver">IFaxServer</a>
