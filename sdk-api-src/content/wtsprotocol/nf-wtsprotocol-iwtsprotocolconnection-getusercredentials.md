---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetUserCredentials
title: IWTSProtocolConnection::GetUserCredentials (wtsprotocol.h)
author: windows-sdk-content
description: IWTSProtocolConnection::GetUserCredentials is no longer available. Instead, use IWRdsProtocolConnection::GetUserCredentials.
old-location: termserv\iwtsprotocolconnection_getusercredentials.htm
tech.root: TermServ
ms.assetid: 48cd1a57-5f6d-4feb-889d-7441a76c0410
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetUserCredentials, GetUserCredentials method [Remote Desktop Services], GetUserCredentials method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetUserCredentials method, IWTSProtocolConnection.GetUserCredentials, IWTSProtocolConnection::GetUserCredentials, termserv.iwtsprotocolconnection_getusercredentials, wtsprotocol/IWTSProtocolConnection::GetUserCredentials
ms.topic: method
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
 - IWTSProtocolConnection.GetUserCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolConnection::GetUserCredentials


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::GetUserCredentials</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getusercredentials">IWRdsProtocolConnection::GetUserCredentials</a>.]

Returns user credentials.


## -parameters




### -param pUserCreds [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wtsdefs/ns-wtsdefs-_wts_user_credential">WTS_USER_CREDENTIAL</a> structure that contains the credentials. Currently, only the user name, password, and domain are supported. The user name and password are plaintext.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



If your protocol returns an <b>HRESULT</b> error code, or the user provides incorrect credentials, WinLogon will display a logon screen to request credentials. If your protocol returns <b>S_OK</b>, the credentials will be passed to WinLogon to log on the user.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>
 

 

