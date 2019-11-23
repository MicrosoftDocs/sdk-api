---
UID: NS:wtsdefs._WRDS_LISTENER_SETTINGS
title: WRDS_LISTENER_SETTINGS (wtsdefs.h)

description: Contains listener setting information for a remote session.
old-location: termserv\wrds_listener_settings.htm
tech.root: TermServ
ms.assetid: 75C9C9AF-9C27-402C-886D-269BF567825F

ms.date: 12/05/2018
ms.keywords: '*PWRDS_LISTENER_SETTINGS, PWRDS_LISTENER_SETTINGS, PWRDS_LISTENER_SETTINGS structure pointer [Remote Desktop Services], WRDS_LISTENER_SETTINGS, WRDS_LISTENER_SETTINGS structure [Remote Desktop Services], WRDS_LISTENER_SETTING_LEVEL_1, termserv.wrds_listener_settings, wtsdefs/PWRDS_LISTENER_SETTINGS, wtsdefs/WRDS_LISTENER_SETTINGS'
ms.topic: struct
f1_keywords:
- wtsdefs/WRDS_LISTENER_SETTINGS
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wtsdefs.h
api_name:
- WRDS_LISTENER_SETTINGS
targetos: Windows
req.typenames: WRDS_LISTENER_SETTINGS, *PWRDS_LISTENER_SETTINGS
req.redist: 
ms.custom: 19H1
---

# WRDS_LISTENER_SETTINGS structure


## -description


Contains listener setting information for a remote session.


## -struct-fields




### -field WRdsListenerSettingLevel

A value of the <a href="https://docs.microsoft.com/windows/desktop/api/wtsdefs/ne-wtsdefs-wrds_listener_setting_level">WRDS_LISTENER_SETTING_LEVEL</a> enumeration that specifies the type of structure that is contained in the <b>WRdsListenerSetting</b> member.



#### WRDS_LISTENER_SETTING_LEVEL_1

The structure is a <a href="https://docs.microsoft.com/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_listener_settings_1">WRDS_LISTENER_SETTINGS_1</a> structure.


### -field WRdsListenerSetting

A <a href="https://docs.microsoft.com/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_listener_setting">WRDS_LISTENER_SETTING</a> structure that specifies the listener settings.


### -field WRdsListenerSetting.switch_is

 


### -field WRdsListenerSetting.switch_is.WRdsListenerSettingLevel

 



