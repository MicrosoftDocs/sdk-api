---
UID: NS:winwlx._WLX_CLIENT_CREDENTIALS_INFO
title: WLX_CLIENT_CREDENTIALS_INFO_V1_0 (winwlx.h)
description: Contains the client credentials returned by a call to WlxQueryClientCredentials or WlxQueryInetConnectorCredentials.
helpviewer_keywords: ["*PWLX_CLIENT_CREDENTIALS_INFO_V1_0","PWLX_CLIENT_CREDENTIALS_INFO_V1_0","PWLX_CLIENT_CREDENTIALS_INFO_V1_0 structure pointer [Security]","WLX_CLIENT_CREDENTIALS_INFO_V1_0","WLX_CLIENT_CREDENTIALS_INFO_V1_0 structure [Security]","_gina_wlx_client_credentials_info_v1_0","security.wlx_client_credentials_info_v1_0","winwlx/PWLX_CLIENT_CREDENTIALS_INFO_V1_0","winwlx/WLX_CLIENT_CREDENTIALS_INFO_V1_0"]
old-location: security\wlx_client_credentials_info_v1_0.htm
tech.root: security
ms.assetid: 25fdc00d-e484-415f-8f1b-1f8ed911f9ef
ms.date: 12/05/2018
ms.keywords: '*PWLX_CLIENT_CREDENTIALS_INFO_V1_0, PWLX_CLIENT_CREDENTIALS_INFO_V1_0, PWLX_CLIENT_CREDENTIALS_INFO_V1_0 structure pointer [Security], WLX_CLIENT_CREDENTIALS_INFO_V1_0, WLX_CLIENT_CREDENTIALS_INFO_V1_0 structure [Security], _gina_wlx_client_credentials_info_v1_0, security.wlx_client_credentials_info_v1_0, winwlx/PWLX_CLIENT_CREDENTIALS_INFO_V1_0, winwlx/WLX_CLIENT_CREDENTIALS_INFO_V1_0'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WLX_CLIENT_CREDENTIALS_INFO_V1_0, *PWLX_CLIENT_CREDENTIALS_INFO_V1_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLX_CLIENT_CREDENTIALS_INFO
 - winwlx/_WLX_CLIENT_CREDENTIALS_INFO
 - PWLX_CLIENT_CREDENTIALS_INFO_V1_0
 - winwlx/PWLX_CLIENT_CREDENTIALS_INFO_V1_0
 - WLX_CLIENT_CREDENTIALS_INFO_V1_0
 - winwlx/WLX_CLIENT_CREDENTIALS_INFO_V1_0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winwlx.h
api_name:
 - WLX_CLIENT_CREDENTIALS_INFO_V1_0
---

# WLX_CLIENT_CREDENTIALS_INFO_V1_0 structure


## -description

<p class="CCE_Message">[The WLX_CLIENT_CREDENTIALS_INFO_V1_0 structure is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WLX_CLIENT_CREDENTIALS_INFO_V1_0</b> structure contains the client <a href="/windows/desktop/SecGloss/c-gly">credentials</a> returned by a call to 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a> or 
<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_ic_credentials">WlxQueryInetConnectorCredentials</a>.

This allows a network client session to pass client credentials for automatic logon.
<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a> is called when Terminal Services is enabled.</div><div> </div>The <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL is responsible for calling 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to free the resources used by this structure when the structure is no longer needed.

## -struct-fields

### -field dwType

Specifies the type of <a href="/windows/desktop/SecGloss/c-gly">credentials</a> structure allocated by the GINA DLL. Credential types are defined with the prefix WLX_CREDENTIAL_TYPE_xxx.

### -field pszUserName

A pointer to the name of the account logged onto.

### -field pszDomain

A pointer to the name of the domain used to log on.

### -field pszPassword

A pointer to the plaintext password of the user account. When you have finished using <i>pszPassword</i>, clear the sensitive information from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function.

<b>Windows XP/2000:  </b><a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> is not supported. Overwrite the memory allocated for <i>pszPassword</i> to clear the sensitive information.

For more information about protecting passwords, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -field fPromptForPassword

Forces a prompt for the password due to an administration override. This allows the distinction of auto logon with no password.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a>



<a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_ic_credentials">WlxQueryInetConnectorCredentials</a>