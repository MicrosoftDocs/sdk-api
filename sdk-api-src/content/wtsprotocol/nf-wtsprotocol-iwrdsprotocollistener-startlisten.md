---
UID: NF:wtsprotocol.IWRdsProtocolListener.StartListen
title: IWRdsProtocolListener::StartListen (wtsprotocol.h)
description: Notifies the protocol to start listening for client connection requests.
helpviewer_keywords: ["IWRdsProtocolListener interface [Remote Desktop Services]","StartListen method","IWRdsProtocolListener.StartListen","IWRdsProtocolListener::StartListen","StartListen","StartListen method [Remote Desktop Services]","StartListen method [Remote Desktop Services]","IWRdsProtocolListener interface","termserv.iwrdsprotocollistener_startlisten","wtsprotocol/IWRdsProtocolListener::StartListen"]
old-location: termserv\iwrdsprotocollistener_startlisten.htm
tech.root: TermServ
ms.assetid: d3797411-2ac6-4d3c-8c90-5c566e6d8fa8
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolListener interface [Remote Desktop Services],StartListen method, IWRdsProtocolListener.StartListen, IWRdsProtocolListener::StartListen, StartListen, StartListen method [Remote Desktop Services], StartListen method [Remote Desktop Services],IWRdsProtocolListener interface, termserv.iwrdsprotocollistener_startlisten, wtsprotocol/IWRdsProtocolListener::StartListen
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - IWRdsProtocolListener::StartListen
 - wtsprotocol/IWRdsProtocolListener::StartListen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolListener.StartListen
---

# IWRdsProtocolListener::StartListen


## -description

Notifies the protocol to start listening for client connection requests.

## -parameters

### -param pCallback [in]

A pointer to an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback">IWRdsProtocolListenerCallback</a> object 
implemented by the Remote Desktop Servicesservice. The protocol uses the 
<b>IWRdsProtocolListenerCallback</b> object to notify 
the 

Remote Desktop Services 
service about incoming connection requests. The protocol must add a reference to this object and release it when 
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten">StopListen</a> is called.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, 
return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, 
see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <b>StartListen</b> method is called when the Remote Desktop Services service starts.

<ol>
<li>The Remote Desktop Services service calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> to create an  <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">IWRdsProtocolManager</a> object.</li>
<li>The Remote Desktop Services service calls <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener">CreateListener</a> on the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">IWRdsProtocolManager</a> interface. The protocol creates an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener">IWRdsProtocolListener</a> object and passes it back to the Remote Desktop Services service.</li>
<li>The Remote Desktop Services service calls <b>StartListen</b> on the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener">IWRdsProtocolListener</a> object.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener">IWRdsProtocolListener</a>