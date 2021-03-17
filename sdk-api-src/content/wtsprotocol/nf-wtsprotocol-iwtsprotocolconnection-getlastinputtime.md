---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetLastInputTime
title: IWTSProtocolConnection::GetLastInputTime (wtsprotocol.h)
description: IWTSProtocolConnection::GetLastInputTime is no longer available. Instead, use IWRdsProtocolConnection::GetLastInputTime.
helpviewer_keywords: ["GetLastInputTime","GetLastInputTime method [Remote Desktop Services]","GetLastInputTime method [Remote Desktop Services]","IWTSProtocolConnection interface","IWTSProtocolConnection interface [Remote Desktop Services]","GetLastInputTime method","IWTSProtocolConnection.GetLastInputTime","IWTSProtocolConnection::GetLastInputTime","termserv.iwtsprotocolconnection_getlastinputtime","wtsprotocol/IWTSProtocolConnection::GetLastInputTime"]
old-location: termserv\iwtsprotocolconnection_getlastinputtime.htm
tech.root: TermServ
ms.assetid: 8daecbde-8866-4ae9-a07c-32d28d321392
ms.date: 12/05/2018
ms.keywords: GetLastInputTime, GetLastInputTime method [Remote Desktop Services], GetLastInputTime method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetLastInputTime method, IWTSProtocolConnection.GetLastInputTime, IWTSProtocolConnection::GetLastInputTime, termserv.iwtsprotocolconnection_getlastinputtime, wtsprotocol/IWTSProtocolConnection::GetLastInputTime
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
 - IWTSProtocolConnection::GetLastInputTime
 - wtsprotocol/IWTSProtocolConnection::GetLastInputTime
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
 - IWTSProtocolConnection.GetLastInputTime
---

# IWTSProtocolConnection::GetLastInputTime


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::GetLastInputTime</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getlastinputtime">IWRdsProtocolConnection::GetLastInputTime</a>.]

Returns the last time the protocol received input data.

## -parameters

### -param pLastInputTime [out]

An integer that contains the elapsed time, in milliseconds.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>