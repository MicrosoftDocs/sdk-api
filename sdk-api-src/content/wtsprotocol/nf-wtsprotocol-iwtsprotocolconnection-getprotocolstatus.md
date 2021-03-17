---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetProtocolStatus
title: IWTSProtocolConnection::GetProtocolStatus (wtsprotocol.h)
description: IWTSProtocolConnection::GetProtocolStatus is no longer available. Instead, use IWRdsProtocolConnection::GetProtocolStatus.
helpviewer_keywords: ["GetProtocolStatus","GetProtocolStatus method [Remote Desktop Services]","GetProtocolStatus method [Remote Desktop Services]","IWTSProtocolConnection interface","IWTSProtocolConnection interface [Remote Desktop Services]","GetProtocolStatus method","IWTSProtocolConnection.GetProtocolStatus","IWTSProtocolConnection::GetProtocolStatus","termserv.iwtsprotocolconnection_getprotocolstatus","wtsprotocol/IWTSProtocolConnection::GetProtocolStatus"]
old-location: termserv\iwtsprotocolconnection_getprotocolstatus.htm
tech.root: TermServ
ms.assetid: d224877a-649a-4ac2-a5e7-831592e6a0d9
ms.date: 12/05/2018
ms.keywords: GetProtocolStatus, GetProtocolStatus method [Remote Desktop Services], GetProtocolStatus method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetProtocolStatus method, IWTSProtocolConnection.GetProtocolStatus, IWTSProtocolConnection::GetProtocolStatus, termserv.iwtsprotocolconnection_getprotocolstatus, wtsprotocol/IWTSProtocolConnection::GetProtocolStatus
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
 - IWTSProtocolConnection::GetProtocolStatus
 - wtsprotocol/IWTSProtocolConnection::GetProtocolStatus
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
 - IWTSProtocolConnection.GetProtocolStatus
---

# IWTSProtocolConnection::GetProtocolStatus


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::GetProtocolStatus</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getprotocolstatus">IWRdsProtocolConnection::GetProtocolStatus</a>.]

Retrieves information about the protocol status.

## -parameters

### -param pProtocolStatus [out]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_protocol_status">WTS_PROTOCOL_STATUS</a> structure that contains counter, signal, and cache information for the protocol.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>