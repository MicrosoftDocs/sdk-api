---
UID: NE:wtsdefs._WRDS_LISTENER_SETTING_LEVEL
title: WRDS_LISTENER_SETTING_LEVEL (wtsdefs.h)
description: Used to specify the type of structure that is contained in the WRdsListenerSetting member of the WRDS_LISTENER_SETTINGS structure.
helpviewer_keywords: ["*PWRDS_LISTENER_SETTING_LEVEL","PWRDS_LISTENER_SETTING_LEVEL","PWRDS_LISTENER_SETTING_LEVEL enumeration pointer [Remote Desktop Services]","WRDS_LISTENER_SETTING_LEVEL","WRDS_LISTENER_SETTING_LEVEL enumeration [Remote Desktop Services]","WRDS_LISTENER_SETTING_LEVEL_1","WRDS_LISTENER_SETTING_LEVEL_INVALID","termserv.wrds_listener_setting_level","wtsdefs/PWRDS_LISTENER_SETTING_LEVEL","wtsdefs/WRDS_LISTENER_SETTING_LEVEL","wtsdefs/WRDS_LISTENER_SETTING_LEVEL_1","wtsdefs/WRDS_LISTENER_SETTING_LEVEL_INVALID"]
old-location: termserv\wrds_listener_setting_level.htm
tech.root: TermServ
ms.assetid: 09FF31B5-7566-440D-98BB-96C7A4192C30
ms.date: 12/05/2018
ms.keywords: '*PWRDS_LISTENER_SETTING_LEVEL, PWRDS_LISTENER_SETTING_LEVEL, PWRDS_LISTENER_SETTING_LEVEL enumeration pointer [Remote Desktop Services], WRDS_LISTENER_SETTING_LEVEL, WRDS_LISTENER_SETTING_LEVEL enumeration [Remote Desktop Services], WRDS_LISTENER_SETTING_LEVEL_1, WRDS_LISTENER_SETTING_LEVEL_INVALID, termserv.wrds_listener_setting_level, wtsdefs/PWRDS_LISTENER_SETTING_LEVEL, wtsdefs/WRDS_LISTENER_SETTING_LEVEL, wtsdefs/WRDS_LISTENER_SETTING_LEVEL_1, wtsdefs/WRDS_LISTENER_SETTING_LEVEL_INVALID'
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
req.typenames: WRDS_LISTENER_SETTING_LEVEL, *PWRDS_LISTENER_SETTING_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WRDS_LISTENER_SETTING_LEVEL
 - wtsdefs/_WRDS_LISTENER_SETTING_LEVEL
 - PWRDS_LISTENER_SETTING_LEVEL
 - wtsdefs/PWRDS_LISTENER_SETTING_LEVEL
 - WRDS_LISTENER_SETTING_LEVEL
 - wtsdefs/WRDS_LISTENER_SETTING_LEVEL
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
 - WRDS_LISTENER_SETTING_LEVEL
---

# WRDS_LISTENER_SETTING_LEVEL enumeration


## -description

Used to specify the type of structure that is contained in the <b>WRdsListenerSetting</b> member of the <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_listener_settings">WRDS_LISTENER_SETTINGS</a> structure.

## -enum-fields

### -field WRDS_LISTENER_SETTING_LEVEL_INVALID

The type of structure is not defined.

### -field WRDS_LISTENER_SETTING_LEVEL_1

The structure is a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_listener_settings_1">WRDS_LISTENER_SETTINGS_1</a> structure.