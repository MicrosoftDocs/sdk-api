---
UID: NS:winwlx._WLX_CLIENT_CREDENTIALS_INFO_2_0
title: "_WLX_CLIENT_CREDENTIALS_INFO_2_0"
author: windows-sdk-content
description: Contains the client credentials returned by a call to WlxQueryTsLogonCredentials.
old-location: security\wlx_client_credentials_info_v2_0.htm
tech.root: secauthn
ms.assetid: 74783de8-9134-45d8-a8de-26aec884db4d
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PWLX_CLIENT_CREDENTIALS_INFO_V2_0, PWLX_CLIENT_CREDENTIALS_INFO_V2_0, PWLX_CLIENT_CREDENTIALS_INFO_V2_0 structure pointer [Security], WLX_CLIENT_CREDENTIALS_INFO_V2_0, WLX_CLIENT_CREDENTIALS_INFO_V2_0 structure [Security], _WLX_CLIENT_CREDENTIALS_INFO_2_0, security.wlx_client_credentials_info_v2_0, winwlx/PWLX_CLIENT_CREDENTIALS_INFO_V2_0, winwlx/WLX_CLIENT_CREDENTIALS_INFO_V2_0"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winwlx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - Winwlx.h
api_name:
 - WLX_CLIENT_CREDENTIALS_INFO_V2_0
product: Windows
targetos: Windows
req.typenames: WLX_CLIENT_CREDENTIALS_INFO_V2_0, *PWLX_CLIENT_CREDENTIALS_INFO_V2_0
req.redist: 
---

# _WLX_CLIENT_CREDENTIALS_INFO_2_0 structure


## -description


The <b>WLX_CLIENT_CREDENTIALS_INFO_V2_0</b> structure contains the client <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a> returned by a call to 
<a href="https://msdn.microsoft.com/1365b798-682e-4cdb-b8f5-9e7c65366154">WlxQueryTsLogonCredentials</a>.

The <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL is responsible for calling 
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to free the resources used by this structure when the structure is no longer needed.


## -struct-fields




### -field dwType

Specifies the type of <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a> structure allocated by the GINA DLL. Credential types are defined with the prefix WLX_CREDENTIAL_TYPE_xxx.


### -field pszUserName

A pointer to the name of the account logged onto.


### -field pszDomain

A pointer to the name of the domain used to log on.


### -field pszPassword

A pointer to the plaintext password of the user account. When you have finished using <i>pszPassword</i>, clear the sensitive information from memory by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function.

For more information about protecting passwords, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


### -field fPromptForPassword

Forces a prompt for the password due to an administration override. This allows the distinction of auto logon with no password.


### -field fDisconnectOnLogonFailure

Determines whether GINA allows the user to supply different credentials if the logon fails. If  <i>fDisconnectOnLogonFailure</i> is <b>TRUE</b> and the logon fails, <a href="https://msdn.microsoft.com/7f3996b6-7c99-42c5-a39f-8c67ff19a580">WlxLoggedOutSAS</a> should return WLX_SAS_ACTION_LOGOFF.  This will cause <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> to terminate the session. If <i>fDisconnectOnLogonFailure</i> is <b>FALSE</b> and the logon fails, GINA can allow the user to submit different credentials.


## -see-also




<a href="https://msdn.microsoft.com/1365b798-682e-4cdb-b8f5-9e7c65366154">WlxQueryTsLogonCredentials</a>
 

 

