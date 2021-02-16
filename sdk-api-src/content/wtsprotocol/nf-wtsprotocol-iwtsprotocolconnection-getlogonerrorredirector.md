---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetLogonErrorRedirector
title: IWTSProtocolConnection::GetLogonErrorRedirector (wtsprotocol.h)
description: IWTSProtocolConnection::GetLogonErrorRedirector is no longer available. Instead, use IWRdsProtocolConnection::GetLogonErrorRedirector.
helpviewer_keywords: ["GetLogonErrorRedirector","GetLogonErrorRedirector method [Remote Desktop Services]","GetLogonErrorRedirector method [Remote Desktop Services]","IWTSProtocolConnection interface","IWTSProtocolConnection interface [Remote Desktop Services]","GetLogonErrorRedirector method","IWTSProtocolConnection.GetLogonErrorRedirector","IWTSProtocolConnection::GetLogonErrorRedirector","termserv.iwtsprotocolconnection_getlogonerrorredirector","wtsprotocol/IWTSProtocolConnection::GetLogonErrorRedirector"]
old-location: termserv\iwtsprotocolconnection_getlogonerrorredirector.htm
tech.root: TermServ
ms.assetid: 59bd7d50-2903-42b7-b556-4da7b50d8e7a
ms.date: 12/05/2018
ms.keywords: GetLogonErrorRedirector, GetLogonErrorRedirector method [Remote Desktop Services], GetLogonErrorRedirector method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetLogonErrorRedirector method, IWTSProtocolConnection.GetLogonErrorRedirector, IWTSProtocolConnection::GetLogonErrorRedirector, termserv.iwtsprotocolconnection_getlogonerrorredirector, wtsprotocol/IWTSProtocolConnection::GetLogonErrorRedirector
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
 - IWTSProtocolConnection::GetLogonErrorRedirector
 - wtsprotocol/IWTSProtocolConnection::GetLogonErrorRedirector
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
 - IWTSProtocolConnection.GetLogonErrorRedirector
---

# IWTSProtocolConnection::GetLogonErrorRedirector


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::GetLogonErrorRedirector</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getlogonerrorredirector">IWRdsProtocolConnection::GetLogonErrorRedirector</a>.]

Retrieves an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector">IWTSProtocolLogonErrorRedirector</a> interface that specifies how the protocol should handle client logon errors. The protocol must add a reference to this object before returning, and the Remote Desktop Services service releases the reference when the connection is closed.

## -parameters

### -param ppLogonErrorRedir [out]

Address of a pointer to an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector">IWTSProtocolLogonErrorRedirector</a> interface.

## -remarks

The <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector">IWTSProtocolLogonErrorRedirector</a> interface is implemented by the protocol to receive status and error messages from the Remote Desktop Services service.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>