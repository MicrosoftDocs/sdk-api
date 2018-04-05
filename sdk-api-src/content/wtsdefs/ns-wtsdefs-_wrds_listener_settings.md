---
UID: NS:wtsdefs._WRDS_LISTENER_SETTINGS
title: "_WRDS_LISTENER_SETTINGS"
author: windows-driver-content
description: Contains listener setting information for a remote session.
old-location: termserv\wrds_listener_settings.htm
old-project: TermServ
ms.assetid: 75C9C9AF-9C27-402C-886D-269BF567825F
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWRDS_LISTENER_SETTINGS, PWRDS_LISTENER_SETTINGS, PWRDS_LISTENER_SETTINGS structure pointer [Remote Desktop Services], WRDS_LISTENER_SETTINGS, WRDS_LISTENER_SETTINGS structure [Remote Desktop Services], WRDS_LISTENER_SETTING_LEVEL_1, _WRDS_LISTENER_SETTINGS, termserv.wrds_listener_settings, wtsdefs/PWRDS_LISTENER_SETTINGS, wtsdefs/WRDS_LISTENER_SETTINGS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: WRDS_LISTENER_SETTINGS, *PWRDS_LISTENER_SETTINGS, WRDS_LISTENER_SETTINGS, *PWRDS_LISTENER_SETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wtsdefs.h
api_name:
-	WRDS_LISTENER_SETTINGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WRDS_LISTENER_SETTINGS structure


## -description


Contains listener setting information for a remote session.


## -struct-fields




### -field WRdsListenerSettingLevel

A value of the <a href="https://msdn.microsoft.com/09FF31B5-7566-440D-98BB-96C7A4192C30">WRDS_LISTENER_SETTING_LEVEL</a> enumeration that specifies the type of structure that is contained in the <b>WRdsListenerSetting</b> member.



#### WRDS_LISTENER_SETTING_LEVEL_1

The structure is a <a href="https://msdn.microsoft.com/F8F35CED-16EC-4FBB-A3CA-2A5545A88B4A">WRDS_LISTENER_SETTINGS_1</a> structure.


### -field WRdsListenerSetting

A <a href="https://msdn.microsoft.com/F7EF3E44-70B7-437C-9810-982802F86C77">WRDS_LISTENER_SETTING</a> structure that specifies the listener settings.

