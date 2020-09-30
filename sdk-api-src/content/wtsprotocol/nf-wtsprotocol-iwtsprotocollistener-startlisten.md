---
UID: NF:wtsprotocol.IWTSProtocolListener.StartListen
title: IWTSProtocolListener::StartListen (wtsprotocol.h)
description: IWTSProtocolListener::StartListen is no longer available. Instead, use IWRdsProtocolListener::StartListen.
helpviewer_keywords: ["IWTSProtocolListener interface [Remote Desktop Services]","StartListen method","IWTSProtocolListener.StartListen","IWTSProtocolListener::StartListen","StartListen","StartListen method [Remote Desktop Services]","StartListen method [Remote Desktop Services]","IWTSProtocolListener interface","termserv.iwtsprotocollistener_startlisten","wtsprotocol/IWTSProtocolListener::StartListen"]
old-location: termserv\iwtsprotocollistener_startlisten.htm
tech.root: TermServ
ms.assetid: d922ea90-a4eb-4495-947c-ef33bd81f40a
ms.date: 12/05/2018
ms.keywords: IWTSProtocolListener interface [Remote Desktop Services],StartListen method, IWTSProtocolListener.StartListen, IWTSProtocolListener::StartListen, StartListen, StartListen method [Remote Desktop Services], StartListen method [Remote Desktop Services],IWTSProtocolListener interface, termserv.iwtsprotocollistener_startlisten, wtsprotocol/IWTSProtocolListener::StartListen
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSProtocolListener::StartListen
 - wtsprotocol/IWTSProtocolListener::StartListen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolListener.StartListen
---

# IWTSProtocolListener::StartListen


## -description

<p class="CCE_Message">[<b>IWTSProtocolListener::StartListen</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten">IWRdsProtocolListener::StartListen</a>.]

 Notifies the protocol to start listening for client connection requests.

## -parameters

### -param pCallback [in]

A pointer to an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistenercallback">IWTSProtocolListenerCallback</a> object 
implemented by the Remote Desktop Servicesservice. The protocol uses the 
<b>IWTSProtocolListenerCallback</b> object to notify 
the 

Remote Desktop Services 
service about incoming connection requests. The protocol must add a reference to this object and release it when 
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocollistener-stoplisten">StopListen</a> is called.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, 
return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, 
see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <b>StartListen</b> method is called when the Remote Desktop Services service starts.

<ol>
<li>The Remote Desktop Services service calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> to create an  <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager">IWTSProtocolManager</a> object.</li>
<li>The Remote Desktop Services service calls <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolmanager-createlistener">CreateListener</a> on the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager">IWTSProtocolManager</a> interface. The protocol creates an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener">IWTSProtocolListener</a> object and passes it back to the Remote Desktop Services service.</li>
<li>The Remote Desktop Services service calls <b>StartListen</b> on the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener">IWTSProtocolListener</a> object.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener">IWTSProtocolListener</a>