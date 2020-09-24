---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetLogonErrorRedirector
title: IWRdsProtocolConnection::GetLogonErrorRedirector (wtsprotocol.h)
description: Retrieves an IWRdsProtocolLogonErrorRedirector interface that specifies how the protocol should handle client logon errors.
helpviewer_keywords: ["GetLogonErrorRedirector","GetLogonErrorRedirector method [Remote Desktop Services]","GetLogonErrorRedirector method [Remote Desktop Services]","IWRdsProtocolConnection interface","IWRdsProtocolConnection interface [Remote Desktop Services]","GetLogonErrorRedirector method","IWRdsProtocolConnection.GetLogonErrorRedirector","IWRdsProtocolConnection::GetLogonErrorRedirector","termserv.iwrdsprotocolconnection_getlogonerrorredirector","wtsprotocol/IWRdsProtocolConnection::GetLogonErrorRedirector"]
old-location: termserv\iwrdsprotocolconnection_getlogonerrorredirector.htm
tech.root: TermServ
ms.assetid: 9613330F-B8DE-48C7-892C-FB8F50739C13
ms.date: 12/05/2018
ms.keywords: GetLogonErrorRedirector, GetLogonErrorRedirector method [Remote Desktop Services], GetLogonErrorRedirector method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetLogonErrorRedirector method, IWRdsProtocolConnection.GetLogonErrorRedirector, IWRdsProtocolConnection::GetLogonErrorRedirector, termserv.iwrdsprotocolconnection_getlogonerrorredirector, wtsprotocol/IWRdsProtocolConnection::GetLogonErrorRedirector
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
 - IWRdsProtocolConnection::GetLogonErrorRedirector
 - wtsprotocol/IWRdsProtocolConnection::GetLogonErrorRedirector
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
 - IWRdsProtocolConnection.GetLogonErrorRedirector
---

# IWRdsProtocolConnection::GetLogonErrorRedirector


## -description

Retrieves an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector">IWRdsProtocolLogonErrorRedirector</a> interface that specifies how the protocol should handle client logon errors. The protocol must add a reference to this object before returning, and the Remote Desktop Services service releases the reference when the connection is closed.

## -parameters

### -param ppLogonErrorRedir [out]

Address of a pointer to an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector">IWRdsProtocolLogonErrorRedirector</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

If you do not implement this function, return <b>E_NOTIMPL</b> to indicate that logon errors should not be redirected.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>