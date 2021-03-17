---
UID: NS:winwlx._WLX_NOTIFICATION_INFO
title: WLX_NOTIFICATION_INFO (winwlx.h)
description: This structure stores information about a Winlogon event.
helpviewer_keywords: ["*PWLX_NOTIFICATION_INFO","PWLX_NOTIFICATION_INFO","PWLX_NOTIFICATION_INFO structure pointer [Security]","WLX_NOTIFICATION_INFO","WLX_NOTIFICATION_INFO structure [Security]","_gina_wlx_notification_info","security.wlx_notification_info","winwlx/PWLX_NOTIFICATION_INFO","winwlx/WLX_NOTIFICATION_INFO"]
old-location: security\wlx_notification_info.htm
tech.root: security
ms.assetid: 12584a05-b8dc-40a2-83b7-fbecb93ea6f2
ms.date: 12/05/2018
ms.keywords: '*PWLX_NOTIFICATION_INFO, PWLX_NOTIFICATION_INFO, PWLX_NOTIFICATION_INFO structure pointer [Security], WLX_NOTIFICATION_INFO, WLX_NOTIFICATION_INFO structure [Security], _gina_wlx_notification_info, security.wlx_notification_info, winwlx/PWLX_NOTIFICATION_INFO, winwlx/WLX_NOTIFICATION_INFO'
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
req.typenames: WLX_NOTIFICATION_INFO, *PWLX_NOTIFICATION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLX_NOTIFICATION_INFO
 - winwlx/_WLX_NOTIFICATION_INFO
 - PWLX_NOTIFICATION_INFO
 - winwlx/PWLX_NOTIFICATION_INFO
 - WLX_NOTIFICATION_INFO
 - winwlx/WLX_NOTIFICATION_INFO
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
 - WLX_NOTIFICATION_INFO
---

# WLX_NOTIFICATION_INFO structure


## -description

<p class="CCE_Message">[The WLX_NOTIFICATION_INFO structure is no longer available for use as of Windows Server 2008 and Windows Vista.]

This structure stores information about a <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> event.

## -struct-fields

### -field Size

Indicates the size of the structure, in bytes. Your application can check this value against the structure size to validate the structure.

### -field Flags

Reserved for internal use.

### -field UserName

String that specifies the name of the user currently logged on to the system. If the event occurs before a user logs on, this value is <b>NULL</b>.

### -field Domain

String that specifies the name of the domain the user is currently logged on to. If the event occurs before a user logs on, this value is <b>NULL</b>.

### -field WindowStation

Specifies the name of the window station the user is currently logged on to. If the event occurs before a user logs on, this value is <b>NULL</b>. Note that most configurations use a single, default window station. Some applications, such as 
<a href="/windows/desktop/TermServ/about-terminal-services">About Terminal Services</a>, use multiple window stations.

### -field hToken

A handle to the user's token. This value is <b>NULL</b> if the event occurs before a user logs on.

### -field hDesktop

A handle to the desktop that is currently active.

### -field pStatusCallback

Reserved for internal use.