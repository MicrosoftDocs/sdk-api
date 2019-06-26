---
UID: NF:wtsprotocol.IWTSProtocolLogonErrorRedirector.OnBeginPainting
title: IWTSProtocolLogonErrorRedirector::OnBeginPainting (wtsprotocol.h)
author: windows-sdk-content
description: IWTSProtocolLogonErrorRedirector::OnBeginPainting is no longer available. Instead, use IWRdsProtocolLogonErrorRedirector::OnBeginPainting.
old-location: termserv\iwtsprotocollogonerrorredirector_onbeginpainting.htm
tech.root: TermServ
ms.assetid: 1356deeb-ac4a-4877-95be-9df09f4b0210
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWTSProtocolLogonErrorRedirector interface [Remote Desktop Services],OnBeginPainting method, IWTSProtocolLogonErrorRedirector.OnBeginPainting, IWTSProtocolLogonErrorRedirector::OnBeginPainting, OnBeginPainting, OnBeginPainting method [Remote Desktop Services], OnBeginPainting method [Remote Desktop Services],IWTSProtocolLogonErrorRedirector interface, termserv.iwtsprotocollogonerrorredirector_onbeginpainting, wtsprotocol/IWTSProtocolLogonErrorRedirector::OnBeginPainting
ms.topic: method
f1_keywords: 
 - "wtsprotocol/IWTSProtocolLogonErrorRedirector.OnBeginPainting"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolLogonErrorRedirector.OnBeginPainting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolLogonErrorRedirector::OnBeginPainting


## -description


<p class="CCE_Message">[<b>IWTSProtocolLogonErrorRedirector::OnBeginPainting</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollogonerrorredirector-onbeginpainting">IWRdsProtocolLogonErrorRedirector::OnBeginPainting</a>.]

Notifies the protocol that the logon user interface is ready to begin painting.


## -parameters






## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector">IWTSProtocolLogonErrorRedirector</a>
 

 

