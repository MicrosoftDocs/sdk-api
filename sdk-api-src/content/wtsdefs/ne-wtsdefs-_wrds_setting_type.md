---
UID: NE:wtsdefs._WRDS_SETTING_TYPE
title: "_WRDS_SETTING_TYPE"
author: windows-sdk-content
description: Specifies the category of settings being stored in a WRDS_SETTINGS structure.
old-location: termserv\wrds_setting_type.htm
old-project: TermServ
ms.assetid: 2B8191F8-FF54-4CF6-9239-F9BFA0FA0A6B
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: "*PWRDS_SETTING_TYPE, PWRDS_SETTING_TYPE, PWRDS_SETTING_TYPE enumeration pointer [Remote Desktop Services], WRDS_SETTING_TYPE, WRDS_SETTING_TYPE enumeration [Remote Desktop Services], WRDS_SETTING_TYPE_INVALID, WRDS_SETTING_TYPE_MACHINE, WRDS_SETTING_TYPE_SAM, WRDS_SETTING_TYPE_USER, _WRDS_SETTING_TYPE, termserv.wrds_setting_type, wtsdefs/PWRDS_SETTING_TYPE, wtsdefs/WRDS_SETTING_TYPE, wtsdefs/WRDS_SETTING_TYPE_INVALID, wtsdefs/WRDS_SETTING_TYPE_MACHINE, wtsdefs/WRDS_SETTING_TYPE_SAM, wtsdefs/WRDS_SETTING_TYPE_USER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTS_SESSION_INFO_1W (Unicode) and WTS_SESSION_INFO_1A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WRDS_SETTING_TYPE, *PWRDS_SETTING_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WRDS_SETTING_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WRDS_SETTING_TYPE enumeration


## -description


Specifies the category of settings being stored in a <a href="https://msdn.microsoft.com/38AD33F9-F955-4906-90E2-3FE5261A3E58">WRDS_SETTINGS</a> structure.


## -enum-fields




### -field WRDS_SETTING_TYPE_INVALID

The setting type is not defined.


### -field WRDS_SETTING_TYPE_MACHINE

The settings apply to group policy for the computer.


### -field WRDS_SETTING_TYPE_USER

The settings apply to group policy for the user.


### -field WRDS_SETTING_TYPE_SAM

The settings apply to the user security accounts manager (SAM).

