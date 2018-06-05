---
UID: NS:winwlx._WLX_CLIENT_CREDENTIALS_INFO
title: "_WLX_CLIENT_CREDENTIALS_INFO"
author: windows-sdk-content
description: Contains the client credentials returned by a call to WlxQueryClientCredentials or WlxQueryInetConnectorCredentials.
old-location: security\wlx_client_credentials_info_v1_0.htm
old-project: SecAuthN
ms.assetid: 25fdc00d-e484-415f-8f1b-1f8ed911f9ef
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PWLX_CLIENT_CREDENTIALS_INFO_V1_0, PWLX_CLIENT_CREDENTIALS_INFO_V1_0, PWLX_CLIENT_CREDENTIALS_INFO_V1_0 structure pointer [Security], WLX_CLIENT_CREDENTIALS_INFO_V1_0, WLX_CLIENT_CREDENTIALS_INFO_V1_0 structure [Security], _WLX_CLIENT_CREDENTIALS_INFO, _gina_wlx_client_credentials_info_v1_0, security.wlx_client_credentials_info_v1_0, winwlx/PWLX_CLIENT_CREDENTIALS_INFO_V1_0, winwlx/WLX_CLIENT_CREDENTIALS_INFO_V1_0"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winwlx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: WLX_CLIENT_CREDENTIALS_INFO_V1_0, *PWLX_CLIENT_CREDENTIALS_INFO_V1_0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winwlx.h
api_name:
-	WLX_CLIENT_CREDENTIALS_INFO_V1_0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLX_CLIENT_CREDENTIALS_INFO structure


## -description


<p class="CCE_Message">[The WLX_CLIENT_CREDENTIALS_INFO_V1_0 structure is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WLX_CLIENT_CREDENTIALS_INFO_V1_0</b> structure contains the client <a href="https://msdn.microsoft.com/library/windows/hardware/dn922689">credentials</a> returned by a call to 
<a href="https://msdn.microsoft.com/b563606d-f4d5-48d7-914d-a11ed5f536a1">WlxQueryClientCredentials</a> or 
<a href="https://msdn.microsoft.com/dfa12961-1552-4531-8f79-d44fb2a46e74">WlxQueryInetConnectorCredentials</a>.

This allows a network client session to pass client credentials for automatic logon.
<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/b563606d-f4d5-48d7-914d-a11ed5f536a1">WlxQueryClientCredentials</a> is called when Terminal Services is enabled.</div><div> </div>The <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL is responsible for calling 
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to free the resources used by this structure when the structure is no longer needed.


## -struct-fields




### -field dwType

Specifies the type of <a href="https://msdn.microsoft.com/library/windows/hardware/dn922689">credentials</a> structure allocated by the GINA DLL. Credential types are defined with the prefix WLX_CREDENTIAL_TYPE_xxx.


### -field pszUserName

A pointer to the name of the account logged onto.


### -field pszDomain

A pointer to the name of the domain used to log on.


### -field pszPassword

A pointer to the plaintext password of the user account. When you have finished using <i>pszPassword</i>, clear the sensitive information from memory by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function.

<b>Windows XP/2000:  </b><a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> is not supported. Overwrite the memory allocated for <i>pszPassword</i> to clear the sensitive information.


For more information about protecting passwords, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


### -field fPromptForPassword

Forces a prompt for the password due to an administration override. This allows the distinction of auto logon with no password.


## -see-also




<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>



<a href="https://msdn.microsoft.com/b563606d-f4d5-48d7-914d-a11ed5f536a1">WlxQueryClientCredentials</a>



<a href="https://msdn.microsoft.com/dfa12961-1552-4531-8f79-d44fb2a46e74">WlxQueryInetConnectorCredentials</a>
 

 

