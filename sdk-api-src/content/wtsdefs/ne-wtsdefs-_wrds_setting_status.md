---
UID: NE:wtsdefs._WRDS_SETTING_STATUS
title: "_WRDS_SETTING_STATUS"
author: windows-driver-content
description: Specifies the status of a policy setting for various members of the WRDS_SETTINGS_1 structure.
old-location: termserv\wrds_setting_status.htm
old-project: TermServ
ms.assetid: FA56FDCB-70E7-4D90-99DE-6C624404BEF9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWRDS_SETTING_STATUS, PWRDS_SETTING_STATUS, PWRDS_SETTING_STATUS enumeration pointer [Remote Desktop Services], WRDS_SETTING_STATUS, WRDS_SETTING_STATUS enumeration [Remote Desktop Services], WRDS_SETTING_STATUS_DISABLED, WRDS_SETTING_STATUS_ENABLED, WRDS_SETTING_STATUS_NOTAPPLICABLE, WRDS_SETTING_STATUS_NOTCONFIGURED, _WRDS_SETTING_STATUS, termserv.wrds_setting_status, wtsdefs/PWRDS_SETTING_STATUS, wtsdefs/WRDS_SETTING_STATUS, wtsdefs/WRDS_SETTING_STATUS_DISABLED, wtsdefs/WRDS_SETTING_STATUS_ENABLED, wtsdefs/WRDS_SETTING_STATUS_NOTAPPLICABLE, wtsdefs/WRDS_SETTING_STATUS_NOTCONFIGURED"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WRDS_SETTING_STATUS, *PWRDS_SETTING_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wtsdefs.h
api_name:
-	WRDS_SETTING_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WRDS_SETTING_STATUS enumeration


## -description


Specifies the status of a policy setting for various members of the <a href="https://msdn.microsoft.com/47100A84-49F4-4FF1-8CCB-731638F27C4F">WRDS_SETTINGS_1</a> structure.


## -enum-fields




### -field WRDS_SETTING_STATUS_NOTAPPLICABLE

The setting status has not been defined.


### -field WRDS_SETTING_STATUS_DISABLED

The setting is disabled.


### -field WRDS_SETTING_STATUS_ENABLED

The setting is enabled.


### -field WRDS_SETTING_STATUS_NOTCONFIGURED

The setting is not configured.


## -remarks



The three primary values (disabled, enabled, and not configured) correspond to the states that are available when defining rules in the group policy editor. When the setting status is enabled, the value of the setting can be changed by the corresponding value member within the <a href="https://msdn.microsoft.com/47100A84-49F4-4FF1-8CCB-731638F27C4F">WRDS_SETTINGS_1</a> structure. For example, if that structure's <b>WRdsColorDepthStatus</b> member has a value of <b>WRDS_SETTING_STATUS_ENABLED</b>, the <b>WRdsColorDepthValue</b> member will go into effect. Otherwise, the value member is not used in processing.



