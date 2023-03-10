---
UID: NS:wtsdefs._WRDS_CONNECTION_SETTINGS
title: WRDS_CONNECTION_SETTINGS (wtsdefs.h)
description: Contains connection setting information for a remote session. (WRDS_CONNECTION_SETTINGS)
helpviewer_keywords: ["*PWRDS_CONNECTION_SETTINGS","PWRDS_CONNECTION_SETTINGS","PWRDS_CONNECTION_SETTINGS structure pointer [Remote Desktop Services]","WRDS_CONNECTION_SETTINGS","WRDS_CONNECTION_SETTINGS structure [Remote Desktop Services]","WRDS_CONNECTION_SETTING_LEVEL_1","termserv.wrds_connection_settings","wtsdefs/PWRDS_CONNECTION_SETTINGS","wtsdefs/WRDS_CONNECTION_SETTINGS"]
old-location: termserv\wrds_connection_settings.htm
tech.root: TermServ
ms.assetid: 9219AE45-5F11-484E-BD78-F8E1AB41D648
ms.date: 12/05/2018
ms.keywords: '*PWRDS_CONNECTION_SETTINGS, PWRDS_CONNECTION_SETTINGS, PWRDS_CONNECTION_SETTINGS structure pointer [Remote Desktop Services], WRDS_CONNECTION_SETTINGS, WRDS_CONNECTION_SETTINGS structure [Remote Desktop Services], WRDS_CONNECTION_SETTING_LEVEL_1, termserv.wrds_connection_settings, wtsdefs/PWRDS_CONNECTION_SETTINGS, wtsdefs/WRDS_CONNECTION_SETTINGS'
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
req.typenames: WRDS_CONNECTION_SETTINGS, *PWRDS_CONNECTION_SETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WRDS_CONNECTION_SETTINGS
 - wtsdefs/_WRDS_CONNECTION_SETTINGS
 - PWRDS_CONNECTION_SETTINGS
 - wtsdefs/PWRDS_CONNECTION_SETTINGS
 - WRDS_CONNECTION_SETTINGS
 - wtsdefs/WRDS_CONNECTION_SETTINGS
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
 - WRDS_CONNECTION_SETTINGS
---

# WRDS_CONNECTION_SETTINGS structure


## -description

Contains connection setting information for a remote session.

## -struct-fields

### -field WRdsConnectionSettingLevel

A value of the <a href="/windows/desktop/api/wtsdefs/ne-wtsdefs-wrds_connection_setting_level">WRDS_CONNECTION_SETTING_LEVEL</a> enumeration that specifies the type of structure that is contained in the <b>WRdsConnectionSetting</b> member.



#### WRDS_CONNECTION_SETTING_LEVEL_1

The structure is a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_connection_settings_1">WRDS_CONNECTION_SETTINGS_1</a> structure.

### -field WRdsConnectionSetting

A <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_connection_setting">WRDS_CONNECTION_SETTING</a> structure that specifies the connection settings.



## -see-also

<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-logonnotify">IWRdsProtocolConnection::LogonNotify</a>
