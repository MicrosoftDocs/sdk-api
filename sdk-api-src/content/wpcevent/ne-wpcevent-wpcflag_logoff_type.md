---
UID: NE:wpcevent.tagWPCFLAG_LOGOFF_TYPE
title: WPCFLAG_LOGOFF_TYPE (wpcevent.h)
description: Indicates information about the type of logoff method used.
helpviewer_keywords: ["WPCFLAG_LOGOFF_TYPE","WPCFLAG_LOGOFF_TYPE enumeration","WPCFLAG_LOGOFF_TYPE_FORCEDFUS","WPCFLAG_LOGOFF_TYPE_FUS","WPCFLAG_LOGOFF_TYPE_LOGOUT","WPCFLAG_LOGOFF_TYPE_RESTART","WPCFLAG_LOGOFF_TYPE_SHUTDOWN","parcon.wpcflag_logoff_type","wpcevent/WPCFLAG_LOGOFF_TYPE","wpcevent/WPCFLAG_LOGOFF_TYPE_FORCEDFUS","wpcevent/WPCFLAG_LOGOFF_TYPE_FUS","wpcevent/WPCFLAG_LOGOFF_TYPE_LOGOUT","wpcevent/WPCFLAG_LOGOFF_TYPE_RESTART","wpcevent/WPCFLAG_LOGOFF_TYPE_SHUTDOWN"]
old-location: parcon\wpcflag_logoff_type.htm
tech.root: parcon
ms.assetid: 1c375477-70ab-49da-93d0-d52346d0dc7b
ms.date: 12/05/2018
ms.keywords: WPCFLAG_LOGOFF_TYPE, WPCFLAG_LOGOFF_TYPE enumeration, WPCFLAG_LOGOFF_TYPE_FORCEDFUS, WPCFLAG_LOGOFF_TYPE_FUS, WPCFLAG_LOGOFF_TYPE_LOGOUT, WPCFLAG_LOGOFF_TYPE_RESTART, WPCFLAG_LOGOFF_TYPE_SHUTDOWN, parcon.wpcflag_logoff_type, wpcevent/WPCFLAG_LOGOFF_TYPE, wpcevent/WPCFLAG_LOGOFF_TYPE_FORCEDFUS, wpcevent/WPCFLAG_LOGOFF_TYPE_FUS, wpcevent/WPCFLAG_LOGOFF_TYPE_LOGOUT, wpcevent/WPCFLAG_LOGOFF_TYPE_RESTART, wpcevent/WPCFLAG_LOGOFF_TYPE_SHUTDOWN
req.header: wpcevent.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: WPCFLAG_LOGOFF_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWPCFLAG_LOGOFF_TYPE
 - wpcevent/tagWPCFLAG_LOGOFF_TYPE
 - WPCFLAG_LOGOFF_TYPE
 - wpcevent/WPCFLAG_LOGOFF_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wpcevent.h
api_name:
 - WPCFLAG_LOGOFF_TYPE
---

# WPCFLAG_LOGOFF_TYPE enumeration


## -description

Indicates information about the type of logoff method used.

## -enum-fields

### -field WPCFLAG_LOGOFF_TYPE_LOGOUT:0x00000000

The user logged off by logging off the computer.

### -field WPCFLAG_LOGOFF_TYPE_RESTART:0x00000001

The user logged off by restarting the computer.

### -field WPCFLAG_LOGOFF_TYPE_SHUTDOWN:0x00000002

The user logged off by shutting down the computer.

### -field WPCFLAG_LOGOFF_TYPE_FUS:0x00000004

The user logged off by using fast user switching.

### -field WPCFLAG_LOGOFF_TYPE_FORCEDFUS:0x00000008

The user was forced to log off by fast user switching.

