---
UID: NF:wtsprotocol.IWRdsProtocolConnection.GetUserCredentials
title: IWRdsProtocolConnection::GetUserCredentials
author: windows-sdk-content
description: Returns user credentials.
old-location: termserv\iwrdsprotocolconnection_getusercredentials.htm
old-project: termserv
ms.assetid: dcd8de76-e260-4b3b-98ca-4f486b3b6635
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: GetUserCredentials, GetUserCredentials method [Remote Desktop Services], GetUserCredentials method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],GetUserCredentials method, IWRdsProtocolConnection.GetUserCredentials, IWRdsProtocolConnection::GetUserCredentials, termserv.iwrdsprotocolconnection_getusercredentials, wtsprotocol/IWRdsProtocolConnection::GetUserCredentials
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolConnection.GetUserCredentials
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolConnection::GetUserCredentials


## -description


Returns user credentials.


## -parameters




### -param pUserCreds [out]

A pointer to a <a href="https://msdn.microsoft.com/79474bc1-3626-4c0e-ae63-6180404369ea">WRDS_USER_CREDENTIAL</a> structure that contains the credentials. Currently, only the user name, password, and domain are supported. The user name and password are plaintext.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If your protocol returns an <b>HRESULT</b> error code, or the user provides incorrect credentials, WinLogon will display a logon screen to request credentials. If your protocol returns <b>S_OK</b>, the credentials will be passed to WinLogon to log on the user.




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 

