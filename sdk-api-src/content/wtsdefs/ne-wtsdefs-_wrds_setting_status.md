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



