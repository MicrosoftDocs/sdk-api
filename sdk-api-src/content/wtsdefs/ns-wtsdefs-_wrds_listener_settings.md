---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


### -field WRdsListenerSetting.switch_is

 


### -field WRdsListenerSetting.switch_is.WRdsListenerSettingLevel

 



