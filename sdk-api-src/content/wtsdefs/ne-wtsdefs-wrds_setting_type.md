---
UID: NE:wtsdefs._WRDS_SETTING_TYPE
title: WRDS_SETTING_TYPE (wtsdefs.h)
description: Specifies the category of settings being stored in a WRDS_SETTINGS structure.
helpviewer_keywords: ["*PWRDS_SETTING_TYPE","PWRDS_SETTING_TYPE","PWRDS_SETTING_TYPE enumeration pointer [Remote Desktop Services]","WRDS_SETTING_TYPE","WRDS_SETTING_TYPE enumeration [Remote Desktop Services]","WRDS_SETTING_TYPE_INVALID","WRDS_SETTING_TYPE_MACHINE","WRDS_SETTING_TYPE_SAM","WRDS_SETTING_TYPE_USER","termserv.wrds_setting_type","wtsdefs/PWRDS_SETTING_TYPE","wtsdefs/WRDS_SETTING_TYPE","wtsdefs/WRDS_SETTING_TYPE_INVALID","wtsdefs/WRDS_SETTING_TYPE_MACHINE","wtsdefs/WRDS_SETTING_TYPE_SAM","wtsdefs/WRDS_SETTING_TYPE_USER"]
old-location: termserv\wrds_setting_type.htm
tech.root: TermServ
ms.assetid: 2B8191F8-FF54-4CF6-9239-F9BFA0FA0A6B
ms.date: 12/05/2018
ms.keywords: '*PWRDS_SETTING_TYPE, PWRDS_SETTING_TYPE, PWRDS_SETTING_TYPE enumeration pointer [Remote Desktop Services], WRDS_SETTING_TYPE, WRDS_SETTING_TYPE enumeration [Remote Desktop Services], WRDS_SETTING_TYPE_INVALID, WRDS_SETTING_TYPE_MACHINE, WRDS_SETTING_TYPE_SAM, WRDS_SETTING_TYPE_USER, termserv.wrds_setting_type, wtsdefs/PWRDS_SETTING_TYPE, wtsdefs/WRDS_SETTING_TYPE, wtsdefs/WRDS_SETTING_TYPE_INVALID, wtsdefs/WRDS_SETTING_TYPE_MACHINE, wtsdefs/WRDS_SETTING_TYPE_SAM, wtsdefs/WRDS_SETTING_TYPE_USER'
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
req.typenames: WRDS_SETTING_TYPE, *PWRDS_SETTING_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WRDS_SETTING_TYPE
 - wtsdefs/_WRDS_SETTING_TYPE
 - PWRDS_SETTING_TYPE
 - wtsdefs/PWRDS_SETTING_TYPE
 - WRDS_SETTING_TYPE
 - wtsdefs/WRDS_SETTING_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WRDS_SETTING_TYPE
---

# WRDS_SETTING_TYPE enumeration


## -description

Specifies the category of settings being stored in a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_settings">WRDS_SETTINGS</a> structure.

## -enum-fields

### -field WRDS_SETTING_TYPE_INVALID

The setting type is not defined.

### -field WRDS_SETTING_TYPE_MACHINE

The settings apply to group policy for the computer.

### -field WRDS_SETTING_TYPE_USER

The settings apply to group policy for the user.

### -field WRDS_SETTING_TYPE_SAM

The settings apply to the user security accounts manager (SAM).