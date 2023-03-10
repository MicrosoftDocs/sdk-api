---
UID: NF:wtsprotocol.IWRdsProtocolConnection.SetErrorInfo
title: IWRdsProtocolConnection::SetErrorInfo (wtsprotocol.h)
description: Sets error information in the protocol.
helpviewer_keywords: ["IWRdsProtocolConnection interface [Remote Desktop Services]","SetErrorInfo method","IWRdsProtocolConnection.SetErrorInfo","IWRdsProtocolConnection::SetErrorInfo","SetErrorInfo","SetErrorInfo method [Remote Desktop Services]","SetErrorInfo method [Remote Desktop Services]","IWRdsProtocolConnection interface","termserv.iwrdsprotocolconnection_seterrorinfo","wtsprotocol/IWRdsProtocolConnection::SetErrorInfo"]
old-location: termserv\iwrdsprotocolconnection_seterrorinfo.htm
tech.root: TermServ
ms.assetid: 114abaf1-fe67-4d80-ad5d-f49aac9dd587
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolConnection interface [Remote Desktop Services],SetErrorInfo method, IWRdsProtocolConnection.SetErrorInfo, IWRdsProtocolConnection::SetErrorInfo, SetErrorInfo, SetErrorInfo method [Remote Desktop Services], SetErrorInfo method [Remote Desktop Services],IWRdsProtocolConnection interface, termserv.iwrdsprotocolconnection_seterrorinfo, wtsprotocol/IWRdsProtocolConnection::SetErrorInfo
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
 - IWRdsProtocolConnection::SetErrorInfo
 - wtsprotocol/IWRdsProtocolConnection::SetErrorInfo
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
 - IWRdsProtocolConnection.SetErrorInfo
---

# IWRdsProtocolConnection::SetErrorInfo


## -description

Sets error information in the protocol.

## -parameters

### -param ulError [in]

The error code.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>