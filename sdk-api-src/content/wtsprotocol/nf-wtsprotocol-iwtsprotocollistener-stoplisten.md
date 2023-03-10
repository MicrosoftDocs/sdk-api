---
UID: NF:wtsprotocol.IWTSProtocolListener.StopListen
title: IWTSProtocolListener::StopListen (wtsprotocol.h)
description: IWTSProtocolListener::StopListen is no longer available. Instead, use IWRdsProtocolListener::StopListen.
helpviewer_keywords: ["IWTSProtocolListener interface [Remote Desktop Services]","StopListen method","IWTSProtocolListener.StopListen","IWTSProtocolListener::StopListen","StopListen","StopListen method [Remote Desktop Services]","StopListen method [Remote Desktop Services]","IWTSProtocolListener interface","termserv.iwtsprotocollistener_stoplisten","wtsprotocol/IWTSProtocolListener::StopListen"]
old-location: termserv\iwtsprotocollistener_stoplisten.htm
tech.root: TermServ
ms.assetid: 5c5b09d3-74d6-4067-b18b-ed2a54af4153
ms.date: 12/05/2018
ms.keywords: IWTSProtocolListener interface [Remote Desktop Services],StopListen method, IWTSProtocolListener.StopListen, IWTSProtocolListener::StopListen, StopListen, StopListen method [Remote Desktop Services], StopListen method [Remote Desktop Services],IWTSProtocolListener interface, termserv.iwtsprotocollistener_stoplisten, wtsprotocol/IWTSProtocolListener::StopListen
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
 - IWTSProtocolListener::StopListen
 - wtsprotocol/IWTSProtocolListener::StopListen
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
 - IWTSProtocolListener.StopListen
---

# IWTSProtocolListener::StopListen


## -description

<p class="CCE_Message">[<b>IWTSProtocolListener::StopListen</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten">IWRdsProtocolListener::StopListen</a>.]

Notifies the protocol to stop listening for client connection requests.



## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener">IWTSProtocolListener</a>
