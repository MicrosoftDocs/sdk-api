---
UID: NS:wtsdefs._WRDS_CONNECTION_SETTINGS
title: WRDS_CONNECTION_SETTINGS
author: windows-sdk-content
description: Contains connection setting information for a remote session.
old-location: termserv\wrds_connection_settings.htm
tech.root: TermServ
ms.assetid: 9219AE45-5F11-484E-BD78-F8E1AB41D648
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWRDS_CONNECTION_SETTINGS, PWRDS_CONNECTION_SETTINGS, PWRDS_CONNECTION_SETTINGS structure pointer [Remote Desktop Services], WRDS_CONNECTION_SETTINGS, WRDS_CONNECTION_SETTINGS structure [Remote Desktop Services], WRDS_CONNECTION_SETTING_LEVEL_1, termserv.wrds_connection_settings, wtsdefs/PWRDS_CONNECTION_SETTINGS, wtsdefs/WRDS_CONNECTION_SETTINGS"
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
 - WRDS_CONNECTION_SETTINGS
product: Windows
targetos: Windows
req.typenames: WRDS_CONNECTION_SETTINGS, *PWRDS_CONNECTION_SETTINGS
req.redist: 
---

# WRDS_CONNECTION_SETTINGS structure


## -description


Contains connection setting information for a remote session.


## -struct-fields




### -field WRdsConnectionSettingLevel

A value of the <a href="https://msdn.microsoft.com/0D82D26F-1EA6-45A5-90DF-80BE144DC3BF">WRDS_CONNECTION_SETTING_LEVEL</a> enumeration that specifies the type of structure that is contained in the <b>WRdsConnectionSetting</b> member.



#### WRDS_CONNECTION_SETTING_LEVEL_1

The structure is a <a href="https://msdn.microsoft.com/93D4C843-7974-4287-9222-B90206DE6B75">WRDS_CONNECTION_SETTINGS_1</a> structure.


### -field WRdsConnectionSetting

A <a href="https://msdn.microsoft.com/15991230-DBF9-4D32-A65A-1D67D1804D05">WRDS_CONNECTION_SETTING</a> structure that specifies the connection settings.


### -field WRdsConnectionSetting.switch_is

 


### -field WRdsConnectionSetting.switch_is.WRdsConnectionSettingLevel

 




## -see-also




<a href="https://msdn.microsoft.com/2b6ce1cd-0e9f-465d-a5d6-e0d35bddebc4">IWRdsProtocolConnection::LogonNotify</a>
 

 

