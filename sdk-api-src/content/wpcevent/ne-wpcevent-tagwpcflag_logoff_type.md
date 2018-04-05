---
UID: NE:wpcevent.tagWPCFLAG_LOGOFF_TYPE
title: tagWPCFLAG_LOGOFF_TYPE
author: windows-driver-content
description: Indicates information about the type of logoff method used.
old-location: parcon\wpcflag_logoff_type.htm
old-project: parcon
ms.assetid: 1c375477-70ab-49da-93d0-d52346d0dc7b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WPCFLAG_LOGOFF_TYPE, WPCFLAG_LOGOFF_TYPE enumeration, WPCFLAG_LOGOFF_TYPE_FORCEDFUS, WPCFLAG_LOGOFF_TYPE_FUS, WPCFLAG_LOGOFF_TYPE_LOGOUT, WPCFLAG_LOGOFF_TYPE_RESTART, WPCFLAG_LOGOFF_TYPE_SHUTDOWN, parcon.wpcflag_logoff_type, tagWPCFLAG_LOGOFF_TYPE, wpcevent/WPCFLAG_LOGOFF_TYPE, wpcevent/WPCFLAG_LOGOFF_TYPE_FORCEDFUS, wpcevent/WPCFLAG_LOGOFF_TYPE_FUS, wpcevent/WPCFLAG_LOGOFF_TYPE_LOGOUT, wpcevent/WPCFLAG_LOGOFF_TYPE_RESTART, wpcevent/WPCFLAG_LOGOFF_TYPE_SHUTDOWN
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: WPCFLAG_LOGOFF_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wpcevent.h
api_name:
-	WPCFLAG_LOGOFF_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagWPCFLAG_LOGOFF_TYPE enumeration


## -description


Indicates information about the type of logoff method used.


## -enum-fields




### -field WPCFLAG_LOGOFF_TYPE_LOGOUT

The user logged off by logging off the computer.


### -field WPCFLAG_LOGOFF_TYPE_RESTART

The user logged off by restarting the computer.


### -field WPCFLAG_LOGOFF_TYPE_SHUTDOWN

The user logged off by shutting down the computer.


### -field WPCFLAG_LOGOFF_TYPE_FUS

The user logged off by using fast user switching.


### -field WPCFLAG_LOGOFF_TYPE_FORCEDFUS

The user was forced to log off by fast user switching.

