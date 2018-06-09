---
UID: NF:wtsprotocol.IWTSProtocolConnection.GetUserCredentials
title: IWTSProtocolConnection::GetUserCredentials
author: windows-sdk-content
description: IWTSProtocolConnection::GetUserCredentials is no longer available. Instead, use IWRdsProtocolConnection::GetUserCredentials.
old-location: termserv\iwtsprotocolconnection_getusercredentials.htm
old-project: TermServ
ms.assetid: 48cd1a57-5f6d-4feb-889d-7441a76c0410
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetUserCredentials, GetUserCredentials method [Remote Desktop Services], GetUserCredentials method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],GetUserCredentials method, IWTSProtocolConnection.GetUserCredentials, IWTSProtocolConnection::GetUserCredentials, termserv.iwtsprotocolconnection_getusercredentials, wtsprotocol/IWTSProtocolConnection::GetUserCredentials
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolConnection::GetUserCredentials


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::GetUserCredentials</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/dcd8de76-e260-4b3b-98ca-4f486b3b6635">IWRdsProtocolConnection::GetUserCredentials</a>.]

Returns user credentials.


## -parameters




### -param pUserCreds [out]

A pointer to a <a href="https://msdn.microsoft.com/79474bc1-3626-4c0e-ae63-6180404369ea">WTS_USER_CREDENTIAL</a> structure that contains the credentials. Currently, only the user name, password, and domain are supported. The user name and password are plaintext.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



If your protocol returns an <b>HRESULT</b> error code, or the user provides incorrect credentials, WinLogon will display a logon screen to request credentials. If your protocol returns <b>S_OK</b>, the credentials will be passed to WinLogon to log on the user.




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

