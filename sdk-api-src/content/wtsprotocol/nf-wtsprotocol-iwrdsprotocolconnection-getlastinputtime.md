---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetLastInputTime
title: IWRdsProtocolConnection::GetLastInputTime (wtsprotocol.h)
description: Retrieves the last time the protocol received user input.
helpviewer_keywords: ["GetLastInputTime","GetLastInputTime method [Remote Desktop Services]","GetLastInputTime method [Remote Desktop Services]","IWRdsProtocolConnection interface","IWRdsProtocolConnection interface [Remote Desktop Services]","GetLastInputTime method","IWRdsProtocolConnection.GetLastInputTime","IWRdsProtocolConnection::GetLastInputTime","termserv.iwrdsprotocolconnection_getlastinputtime","wtsprotocol/IWRdsProtocolConnection::GetLastInputTime"]
old-location: termserv\iwrdsprotocolconnection_getlastinputtime.htm
tech.root: TermServ
ms.assetid: 1a6acbd2-6155-4513-8892-50a4552abb12
ms.date: 12/05/2018
ms.keywords: GetLastInputTime, GetLastInputTime method [Remote Desktop Services], GetLastInputTime method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetLastInputTime method, IWRdsProtocolConnection.GetLastInputTime, IWRdsProtocolConnection::GetLastInputTime, termserv.iwrdsprotocolconnection_getlastinputtime, wtsprotocol/IWRdsProtocolConnection::GetLastInputTime
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
 - IWRdsProtocolConnection::GetLastInputTime
 - wtsprotocol/IWRdsProtocolConnection::GetLastInputTime
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
 - IWRdsProtocolConnection.GetLastInputTime
---

# IWRdsProtocolConnection::GetLastInputTime


## -description

Retrieves the last time the protocol received user input.

## -parameters

### -param pLastInputTime [out]

A pointer to a <b>ULONG64</b> value that receives the number of milliseconds that has elapsed since the protocol last received input.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>