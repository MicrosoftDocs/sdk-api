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

# _WRDS_CONNECTION_SETTINGS structure


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
 

 

