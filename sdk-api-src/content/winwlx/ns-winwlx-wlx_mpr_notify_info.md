---
UID: NS:winwlx._WLX_MPR_NOTIFY_INFO
title: WLX_MPR_NOTIFY_INFO (winwlx.h)
description: Provides identification and authentication information to network providers.
helpviewer_keywords: ["*PWLX_MPR_NOTIFY_INFO","PWLX_MPR_NOTIFY_INFO","PWLX_MPR_NOTIFY_INFO structure pointer [Security]","WLX_MPR_NOTIFY_INFO","WLX_MPR_NOTIFY_INFO structure [Security]","_gina_wlx_mpr_notify_info","security.wlx_mpr_notify_info","winwlx/PWLX_MPR_NOTIFY_INFO","winwlx/WLX_MPR_NOTIFY_INFO"]
old-location: security\wlx_mpr_notify_info.htm
tech.root: security
ms.assetid: 68098b26-c58d-45fb-aebe-780a73cded80
ms.date: 12/05/2018
ms.keywords: '*PWLX_MPR_NOTIFY_INFO, PWLX_MPR_NOTIFY_INFO, PWLX_MPR_NOTIFY_INFO structure pointer [Security], WLX_MPR_NOTIFY_INFO, WLX_MPR_NOTIFY_INFO structure [Security], _gina_wlx_mpr_notify_info, security.wlx_mpr_notify_info, winwlx/PWLX_MPR_NOTIFY_INFO, winwlx/WLX_MPR_NOTIFY_INFO'
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
req.typenames: WLX_MPR_NOTIFY_INFO, *PWLX_MPR_NOTIFY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLX_MPR_NOTIFY_INFO
 - winwlx/_WLX_MPR_NOTIFY_INFO
 - PWLX_MPR_NOTIFY_INFO
 - winwlx/PWLX_MPR_NOTIFY_INFO
 - WLX_MPR_NOTIFY_INFO
 - winwlx/WLX_MPR_NOTIFY_INFO
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
 - WLX_MPR_NOTIFY_INFO
---

# WLX_MPR_NOTIFY_INFO structure


## -description

<p class="CCE_Message">[The WLX_MPR_NOTIFY_INFO structure is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WLX_MPR_NOTIFY_INFO</b> structure provides identification and authentication information to network providers.

 Your <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL returns this information to Winlogon following a successful authentication. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> is responsible for freeing both the main structure and all strings pointed to from within the structure.

## -struct-fields

### -field pszUserName

A pointer to the name of the account logged onto (for example "user_name"). 




The string pointed to by <b>pszUserName</b> must be separately allocated by your GINA DLL. It will be deallocated by Winlogon.

### -field pszDomain

A pointer to the name of the domain used to log on. 




The string pointed to by pszDomain must be separately allocated by your GINA DLL. It will be deallocated by Winlogon.

### -field pszPassword

A pointer to the plaintext password of the user account. If <b>pszOldPassword</b> is not <b>NULL</b>, <b>pszPassword</b> contains the new password from a password-change operation. 




The string pointed to by <b>pszPassword</b> must be separately allocated by your GINA DLL. It will be deallocated by Winlogon.

 For information about protecting passwords, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -field pszOldPassword

A pointer to the plaintext old password of the user account whose password has just been changed (in this case, <i>pszPassword</i> contains the new password). 




The string pointed to by <b>pszOldPassword</b> must be separately allocated by your GINA DLL. It will be deallocated by Winlogon.