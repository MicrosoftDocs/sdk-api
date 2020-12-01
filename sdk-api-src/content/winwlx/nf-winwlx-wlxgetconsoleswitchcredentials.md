---
UID: NF:winwlx.WlxGetConsoleSwitchCredentials
title: WlxGetConsoleSwitchCredentials function (winwlx.h)
description: Winlogon calls this function to read the currently logged on user's credentials to transparently transfer them to a target session.
helpviewer_keywords: ["WlxGetConsoleSwitchCredentials","WlxGetConsoleSwitchCredentials function [Security]","_gina_wlxgetconsoleswitchcredentials","security.wlxgetconsoleswitchcredentials","winwlx/WlxGetConsoleSwitchCredentials"]
old-location: security\wlxgetconsoleswitchcredentials.htm
tech.root: security
ms.assetid: ee6b3d03-11c9-4eb3-8c76-7041dddc755d
ms.date: 12/05/2018
ms.keywords: WlxGetConsoleSwitchCredentials, WlxGetConsoleSwitchCredentials function [Security], _gina_wlxgetconsoleswitchcredentials, security.wlxgetconsoleswitchcredentials, winwlx/WlxGetConsoleSwitchCredentials
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
 - WlxGetConsoleSwitchCredentials
 - winwlx/WlxGetConsoleSwitchCredentials
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winwlx.h
api_name:
 - WlxGetConsoleSwitchCredentials
---

# WlxGetConsoleSwitchCredentials function


## -description

The <b>WlxGetConsoleSwitchCredentials</b> function must be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function to read the currently logged on user's credentials to transparently transfer them to a target session.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pWlxContext [in]

Pointer to a GINA-specific context.

### -param pCredInfo [out]

Pointer to a <a href="/windows/win32/api/winwlx/ns-winwlx-wlx_consoleswitch_credentials_info_v1_0">WLX_CONSOLESWITCH_CREDENTIALS_INFO_V1_0</a> to return GINA relevant information.

## -returns

Returns <b>TRUE</b> on success and <b>FALSE</b> on failure.