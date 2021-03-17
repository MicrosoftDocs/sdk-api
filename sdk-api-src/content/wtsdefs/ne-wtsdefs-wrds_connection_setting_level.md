---
UID: NE:wtsdefs._WRDS_CONNECTION_SETTING_LEVEL
title: WRDS_CONNECTION_SETTING_LEVEL (wtsdefs.h)
description: Specifies the type of structure contained in the WRdsConnectionSetting member of the WRDS_CONNECTION_SETTINGS structure.
helpviewer_keywords: ["*PWRDS_CONNECTION_SETTING_LEVEL","PWRDS_CONNECTION_SETTING_LEVEL","PWRDS_CONNECTION_SETTING_LEVEL enumeration pointer [Remote Desktop Services]","WRDS_CONNECTION_SETTING_LEVEL","WRDS_CONNECTION_SETTING_LEVEL enumeration [Remote Desktop Services]","WRDS_CONNECTION_SETTING_LEVEL_1","WRDS_CONNECTION_SETTING_LEVEL_INVALID","termserv.wrds_connection_setting_level","wtsdefs/PWRDS_CONNECTION_SETTING_LEVEL","wtsdefs/WRDS_CONNECTION_SETTING_LEVEL","wtsdefs/WRDS_CONNECTION_SETTING_LEVEL_1","wtsdefs/WRDS_CONNECTION_SETTING_LEVEL_INVALID"]
old-location: termserv\wrds_connection_setting_level.htm
tech.root: TermServ
ms.assetid: 0D82D26F-1EA6-45A5-90DF-80BE144DC3BF
ms.date: 12/05/2018
ms.keywords: '*PWRDS_CONNECTION_SETTING_LEVEL, PWRDS_CONNECTION_SETTING_LEVEL, PWRDS_CONNECTION_SETTING_LEVEL enumeration pointer [Remote Desktop Services], WRDS_CONNECTION_SETTING_LEVEL, WRDS_CONNECTION_SETTING_LEVEL enumeration [Remote Desktop Services], WRDS_CONNECTION_SETTING_LEVEL_1, WRDS_CONNECTION_SETTING_LEVEL_INVALID, termserv.wrds_connection_setting_level, wtsdefs/PWRDS_CONNECTION_SETTING_LEVEL, wtsdefs/WRDS_CONNECTION_SETTING_LEVEL, wtsdefs/WRDS_CONNECTION_SETTING_LEVEL_1, wtsdefs/WRDS_CONNECTION_SETTING_LEVEL_INVALID'
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
req.typenames: WRDS_CONNECTION_SETTING_LEVEL, *PWRDS_CONNECTION_SETTING_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WRDS_CONNECTION_SETTING_LEVEL
 - wtsdefs/_WRDS_CONNECTION_SETTING_LEVEL
 - PWRDS_CONNECTION_SETTING_LEVEL
 - wtsdefs/PWRDS_CONNECTION_SETTING_LEVEL
 - WRDS_CONNECTION_SETTING_LEVEL
 - wtsdefs/WRDS_CONNECTION_SETTING_LEVEL
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
 - WRDS_CONNECTION_SETTING_LEVEL
---

# WRDS_CONNECTION_SETTING_LEVEL enumeration


## -description

Specifies the type of structure contained in the <b>WRdsConnectionSetting</b> member of the <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_connection_settings">WRDS_CONNECTION_SETTINGS</a> structure.

## -enum-fields

### -field WRDS_CONNECTION_SETTING_LEVEL_INVALID

The type of structure is not defined.

### -field WRDS_CONNECTION_SETTING_LEVEL_1

The structure is a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_connection_settings_1">WRDS_CONNECTION_SETTINGS_1</a> structure.