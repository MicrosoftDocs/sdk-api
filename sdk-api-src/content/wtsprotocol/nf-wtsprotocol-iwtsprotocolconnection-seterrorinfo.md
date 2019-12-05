---
UID: NF:wtsprotocol.IWTSProtocolConnection.SetErrorInfo
title: IWTSProtocolConnection::SetErrorInfo (wtsprotocol.h)
description: IWTSProtocolConnection::SetErrorInfo is no longer available. Instead, use IWRdsProtocolConnection::SetErrorInfo.
old-location: termserv\iwtsprotocolconnection_seterrorinfo.htm
tech.root: TermServ
ms.assetid: 0ec35560-5aad-403a-9477-50e48ee7136a
ms.date: 12/05/2018
ms.keywords: IWTSProtocolConnection interface [Remote Desktop Services],SetErrorInfo method, IWTSProtocolConnection.SetErrorInfo, IWTSProtocolConnection::SetErrorInfo, SetErrorInfo, SetErrorInfo method [Remote Desktop Services], SetErrorInfo method [Remote Desktop Services],IWTSProtocolConnection interface, termserv.iwtsprotocolconnection_seterrorinfo, wtsprotocol/IWTSProtocolConnection::SetErrorInfo
ms.topic: method
f1_keywords:
- wtsprotocol/IWTSProtocolConnection.SetErrorInfo
dev_langs:
- c++
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
- IWTSProtocolConnection.SetErrorInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolConnection::SetErrorInfo


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::SetErrorInfo</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-seterrorinfo">IWRdsProtocolConnection::SetErrorInfo</a>.]

Sends an error code to the client.


## -parameters




### -param ulError [in]

An integer that contains the error code.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>
 

 

