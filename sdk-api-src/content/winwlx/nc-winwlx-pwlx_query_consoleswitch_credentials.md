---
UID: NC:winwlx.PWLX_QUERY_CONSOLESWITCH_CREDENTIALS
title: PWLX_QUERY_CONSOLESWITCH_CREDENTIALS (winwlx.h)
description: Called by GINA to read the credentials transferred from the Winlogon of the temporary session to the Winlogon of the destination session.
helpviewer_keywords: ["PWLX_QUERY_CONSOLESWITCH_CREDENTIALS","PWLX_QUERY_CONSOLESWITCH_CREDENTIALS callback","WlxQueryConsoleSwitchCredentials","WlxQueryConsoleSwitchCredentials callback function [Security]","_gina_wlxqueryconsoleswitchcredentials","security.wlxqueryconsoleswitchcredentials","winwlx/WlxQueryConsoleSwitchCredentials"]
old-location: security\wlxqueryconsoleswitchcredentials.htm
tech.root: security
ms.assetid: cbb9342e-c06a-4040-9c6c-c761195734a4
ms.date: 12/05/2018
ms.keywords: PWLX_QUERY_CONSOLESWITCH_CREDENTIALS, PWLX_QUERY_CONSOLESWITCH_CREDENTIALS callback, WlxQueryConsoleSwitchCredentials, WlxQueryConsoleSwitchCredentials callback function [Security], _gina_wlxqueryconsoleswitchcredentials, security.wlxqueryconsoleswitchcredentials, winwlx/WlxQueryConsoleSwitchCredentials
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PWLX_QUERY_CONSOLESWITCH_CREDENTIALS
 - winwlx/PWLX_QUERY_CONSOLESWITCH_CREDENTIALS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - winwlx.h
api_name:
 - WlxQueryConsoleSwitchCredentials
---

# PWLX_QUERY_CONSOLESWITCH_CREDENTIALS callback function


## -description

Called by <a href="/windows/desktop/SecGloss/g-gly">GINA</a> to read the credentials transferred from the Winlogon of the temporary session to the Winlogon of the destination session.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pCred [out]

Pointer to a 
<a href="/windows/win32/api/winwlx/ns-winwlx-wlx_consoleswitch_credentials_info_v1_0">WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0</a> structure to be filled with credentials information.

## -returns

Returns <b>TRUE</b> if credentials were transferred and <b>FALSE</b> if the transfer failed.

## -remarks

In order to access this function, the GINA DLL must use the 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_dispatch_version_1_4">WLX_DISPATCH_VERSION_1_4</a> structure.