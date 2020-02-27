---
UID: NF:wtsprotocol.IWRdsProtocolConnectionCallback.GetConnectionId
title: IWRdsProtocolConnectionCallback::GetConnectionId (wtsprotocol.h)
description: Retrieves the connection identifier.
old-location: termserv\iwrdsprotocolconnectioncallback_getconnectionid.htm
tech.root: TermServ
ms.assetid: 2EE03CA1-25D5-4B03-A2F1-EC167BD694B3
ms.date: 12/05/2018
ms.keywords: GetConnectionId, GetConnectionId method [Remote Desktop Services], GetConnectionId method [Remote Desktop Services],IWRdsProtocolConnectionCallback interface, IWRdsProtocolConnectionCallback interface [Remote Desktop Services],GetConnectionId method, IWRdsProtocolConnectionCallback.GetConnectionId, IWRdsProtocolConnectionCallback::GetConnectionId, termserv.iwrdsprotocolconnectioncallback_getconnectionid, wtsprotocol/IWRdsProtocolConnectionCallback::GetConnectionId
f1_keywords:
- wtsprotocol/IWRdsProtocolConnectionCallback.GetConnectionId
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wtsprotocol.h
api_name:
- IWRdsProtocolConnectionCallback.GetConnectionId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolConnectionCallback::GetConnectionId


## -description


Retrieves the connection identifier.


## -parameters




### -param pConnectionId [out]

The address of a <b>ULONG</b> variable that receives the connection identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback">IWRdsProtocolConnectionCallback</a>
 

 

