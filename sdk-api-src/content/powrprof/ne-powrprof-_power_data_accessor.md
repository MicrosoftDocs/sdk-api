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

# _POWER_DATA_ACCESSOR enumeration


## -description


Enumeration values used by <a href="https://msdn.microsoft.com/5b2c8263-d916-4909-be56-ec784537bdc3">PowerEnumerate</a> 
    and <a href="https://msdn.microsoft.com/0b89c189-b162-44d4-aa50-d78385e40c27">PowerSettingAccessCheck</a>.


## -enum-fields




### -field ACCESS_AC_POWER_SETTING_INDEX

Used with <a href="https://msdn.microsoft.com/0b89c189-b162-44d4-aa50-d78385e40c27">PowerSettingAccessCheck</a> to 
      check for group policy overrides for AC power settings.


### -field ACCESS_DC_POWER_SETTING_INDEX

Used with <a href="https://msdn.microsoft.com/0b89c189-b162-44d4-aa50-d78385e40c27">PowerSettingAccessCheck</a> to 
      check for group policy overrides for DC power settings.


### -field ACCESS_FRIENDLY_NAME


### -field ACCESS_DESCRIPTION


### -field ACCESS_POSSIBLE_POWER_SETTING


### -field ACCESS_POSSIBLE_POWER_SETTING_FRIENDLY_NAME


### -field ACCESS_POSSIBLE_POWER_SETTING_DESCRIPTION


### -field ACCESS_DEFAULT_AC_POWER_SETTING


### -field ACCESS_DEFAULT_DC_POWER_SETTING


### -field ACCESS_POSSIBLE_VALUE_MIN


### -field ACCESS_POSSIBLE_VALUE_MAX


### -field ACCESS_POSSIBLE_VALUE_INCREMENT


### -field ACCESS_POSSIBLE_VALUE_UNITS


### -field ACCESS_ICON_RESOURCE


### -field ACCESS_DEFAULT_SECURITY_DESCRIPTOR


### -field ACCESS_ATTRIBUTES


### -field ACCESS_SCHEME

Used to enumerate power schemes with 
      <a href="https://msdn.microsoft.com/5b2c8263-d916-4909-be56-ec784537bdc3">PowerEnumerate</a> and with 
      <a href="https://msdn.microsoft.com/0b89c189-b162-44d4-aa50-d78385e40c27">PowerSettingAccessCheck</a> to check for 
      restricted access to specific power schemes.


### -field ACCESS_SUBGROUP

Used to enumerate subgroups with 
      <a href="https://msdn.microsoft.com/5b2c8263-d916-4909-be56-ec784537bdc3">PowerEnumerate</a>.


### -field ACCESS_INDIVIDUAL_SETTING

Used to enumerate individual power settings with 
      <a href="https://msdn.microsoft.com/5b2c8263-d916-4909-be56-ec784537bdc3">PowerEnumerate</a>.


### -field ACCESS_ACTIVE_SCHEME

Used with <a href="https://msdn.microsoft.com/0b89c189-b162-44d4-aa50-d78385e40c27">PowerSettingAccessCheck</a> to 
      check for group policy overrides for active power schemes.


### -field ACCESS_CREATE_SCHEME

Used with <a href="https://msdn.microsoft.com/0b89c189-b162-44d4-aa50-d78385e40c27">PowerSettingAccessCheck</a> to 
      check for restricted access for creating power schemes.


### -field ACCESS_AC_POWER_SETTING_MAX


### -field ACCESS_DC_POWER_SETTING_MAX


### -field ACCESS_AC_POWER_SETTING_MIN


### -field ACCESS_DC_POWER_SETTING_MIN


### -field ACCESS_PROFILE


### -field ACCESS_OVERLAY_SCHEME


### -field ACCESS_ACTIVE_OVERLAY_SCHEME




## -see-also




<a href="https://msdn.microsoft.com/f78cd97f-586f-4091-ab4a-5f109a0f679a">Power Management Enumeration Types</a>



<a href="https://msdn.microsoft.com/5b2c8263-d916-4909-be56-ec784537bdc3">PowerEnumerate</a>



<a href="https://msdn.microsoft.com/0b89c189-b162-44d4-aa50-d78385e40c27">PowerSettingAccessCheck</a>
 

 

