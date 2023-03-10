---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetUserCredentials
title: IWRdsProtocolConnection::GetUserCredentials (wtsprotocol.h)
description: Returns user credentials.
helpviewer_keywords: ["GetUserCredentials","GetUserCredentials method [Remote Desktop Services]","GetUserCredentials method [Remote Desktop Services]","IWRdsProtocolConnection interface","IWRdsProtocolConnection interface [Remote Desktop Services]","GetUserCredentials method","IWRdsProtocolConnection.GetUserCredentials","IWRdsProtocolConnection::GetUserCredentials","termserv.iwrdsprotocolconnection_getusercredentials","wtsprotocol/IWRdsProtocolConnection::GetUserCredentials"]
old-location: termserv\iwrdsprotocolconnection_getusercredentials.htm
tech.root: TermServ
ms.assetid: dcd8de76-e260-4b3b-98ca-4f486b3b6635
ms.date: 12/05/2018
ms.keywords: GetUserCredentials, GetUserCredentials method [Remote Desktop Services], GetUserCredentials method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetUserCredentials method, IWRdsProtocolConnection.GetUserCredentials, IWRdsProtocolConnection::GetUserCredentials, termserv.iwrdsprotocolconnection_getusercredentials, wtsprotocol/IWRdsProtocolConnection::GetUserCredentials
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
 - IWRdsProtocolConnection::GetUserCredentials
 - wtsprotocol/IWRdsProtocolConnection::GetUserCredentials
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
 - IWRdsProtocolConnection.GetUserCredentials
---

# IWRdsProtocolConnection::GetUserCredentials


## -description

Returns user credentials.

## -parameters

### -param pUserCreds [out]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_user_credential">WRDS_USER_CREDENTIAL</a> structure that contains the credentials. Currently, only the user name, password, and domain are supported. The user name and password are plaintext.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If your protocol returns an <b>HRESULT</b> error code, or the user provides incorrect credentials, WinLogon will display a logon screen to request credentials. If your protocol returns <b>S_OK</b>, the credentials will be passed to WinLogon to log on the user.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>