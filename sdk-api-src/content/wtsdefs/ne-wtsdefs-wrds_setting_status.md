---
UID: NE:wtsdefs._WRDS_SETTING_STATUS
title: WRDS_SETTING_STATUS (wtsdefs.h)
description: Specifies the status of a policy setting for various members of the WRDS_SETTINGS_1 structure.
helpviewer_keywords: ["*PWRDS_SETTING_STATUS","PWRDS_SETTING_STATUS","PWRDS_SETTING_STATUS enumeration pointer [Remote Desktop Services]","WRDS_SETTING_STATUS","WRDS_SETTING_STATUS enumeration [Remote Desktop Services]","WRDS_SETTING_STATUS_DISABLED","WRDS_SETTING_STATUS_ENABLED","WRDS_SETTING_STATUS_NOTAPPLICABLE","WRDS_SETTING_STATUS_NOTCONFIGURED","termserv.wrds_setting_status","wtsdefs/PWRDS_SETTING_STATUS","wtsdefs/WRDS_SETTING_STATUS","wtsdefs/WRDS_SETTING_STATUS_DISABLED","wtsdefs/WRDS_SETTING_STATUS_ENABLED","wtsdefs/WRDS_SETTING_STATUS_NOTAPPLICABLE","wtsdefs/WRDS_SETTING_STATUS_NOTCONFIGURED"]
old-location: termserv\wrds_setting_status.htm
tech.root: TermServ
ms.assetid: FA56FDCB-70E7-4D90-99DE-6C624404BEF9
ms.date: 12/05/2018
ms.keywords: '*PWRDS_SETTING_STATUS, PWRDS_SETTING_STATUS, PWRDS_SETTING_STATUS enumeration pointer [Remote Desktop Services], WRDS_SETTING_STATUS, WRDS_SETTING_STATUS enumeration [Remote Desktop Services], WRDS_SETTING_STATUS_DISABLED, WRDS_SETTING_STATUS_ENABLED, WRDS_SETTING_STATUS_NOTAPPLICABLE, WRDS_SETTING_STATUS_NOTCONFIGURED, termserv.wrds_setting_status, wtsdefs/PWRDS_SETTING_STATUS, wtsdefs/WRDS_SETTING_STATUS, wtsdefs/WRDS_SETTING_STATUS_DISABLED, wtsdefs/WRDS_SETTING_STATUS_ENABLED, wtsdefs/WRDS_SETTING_STATUS_NOTAPPLICABLE, wtsdefs/WRDS_SETTING_STATUS_NOTCONFIGURED'
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
req.typenames: WRDS_SETTING_STATUS, *PWRDS_SETTING_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WRDS_SETTING_STATUS
 - wtsdefs/_WRDS_SETTING_STATUS
 - PWRDS_SETTING_STATUS
 - wtsdefs/PWRDS_SETTING_STATUS
 - WRDS_SETTING_STATUS
 - wtsdefs/WRDS_SETTING_STATUS
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
 - WRDS_SETTING_STATUS
---

# WRDS_SETTING_STATUS enumeration


## -description

Specifies the status of a policy setting for various members of the <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_settings_1">WRDS_SETTINGS_1</a> structure.

## -enum-fields

### -field WRDS_SETTING_STATUS_NOTAPPLICABLE:-1

The setting status has not been defined.

### -field WRDS_SETTING_STATUS_DISABLED

The setting is disabled.

### -field WRDS_SETTING_STATUS_ENABLED

The setting is enabled.

### -field WRDS_SETTING_STATUS_NOTCONFIGURED

The setting is not configured.

## -remarks

The three primary values (disabled, enabled, and not configured) correspond to the states that are available when defining rules in the group policy editor. When the setting status is enabled, the value of the setting can be changed by the corresponding value member within the <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_settings_1">WRDS_SETTINGS_1</a> structure. For example, if that structure's <b>WRdsColorDepthStatus</b> member has a value of <b>WRDS_SETTING_STATUS_ENABLED</b>, the <b>WRdsColorDepthValue</b> member will go into effect. Otherwise, the value member is not used in processing.
