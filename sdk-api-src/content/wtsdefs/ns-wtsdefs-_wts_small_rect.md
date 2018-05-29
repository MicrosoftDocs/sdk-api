---
UID: NS:wtsdefs._WTS_SMALL_RECT
title: "_WTS_SMALL_RECT"
author: windows-sdk-content
description: Contains client window coordinates.
old-location: termserv\wts_small_rect.htm
old-project: TermServ
ms.assetid: 5f139077-8ef4-4c8e-ae33-0dd3aee58ef6
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PWTS_SMALL_RECT, PWRDS_SMALL_RECT, PWRDS_SMALL_RECT structure pointer [Remote Desktop Services], PWTS_SMALL_RECT, PWTS_SMALL_RECT structure pointer [Remote Desktop Services], WRDS_SMALL_RECT, WRDS_SMALL_RECT structure [Remote Desktop Services], WTS_SMALL_RECT, WTS_SMALL_RECT structure [Remote Desktop Services], _WTS_SMALL_RECT, termserv.wts_small_rect, wtsdefs/PWRDS_SMALL_RECT, wtsdefs/PWTS_SMALL_RECT, wtsdefs/WRDS_SMALL_RECT, wtsdefs/WTS_SMALL_RECT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WTS_SMALL_RECT, *PWTS_SMALL_RECT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wtsdefs.h
api_name:
-	WTS_SMALL_RECT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WTS_SMALL_RECT structure


## -description


Contains client window coordinates.


## -struct-fields




### -field Left

Specifies the upper left x-coordinate.


### -field Top

Specifies the upper left y-coordinate.


### -field Right

Specifies the lower right x-coordinate.


### -field Bottom

Specifies the lower right y-coordinate.


## -remarks



This structure is used by the Remote Desktop Services service to redraw the client window.



