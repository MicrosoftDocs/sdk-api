---
UID: NE:powrprof._POWER_DATA_ACCESSOR
title: POWER_DATA_ACCESSOR (powrprof.h)
description: Enumeration values used by PowerEnumerate and PowerSettingAccessCheck.
helpviewer_keywords: ["*PPOWER_DATA_ACCESSOR","ACCESS_ACTIVE_SCHEME","ACCESS_AC_POWER_SETTING_INDEX","ACCESS_CREATE_SCHEME","ACCESS_DC_POWER_SETTING_INDEX","ACCESS_INDIVIDUAL_SETTING","ACCESS_SCHEME","ACCESS_SUBGROUP","POWER_DATA_ACCESSOR","POWER_DATA_ACCESSOR enumeration","PPOWER_DATA_ACCESSOR","PPOWER_DATA_ACCESSOR enumeration pointer","base.power_data_accessor","powrprof/ACCESS_ACTIVE_SCHEME","powrprof/ACCESS_AC_POWER_SETTING_INDEX","powrprof/ACCESS_CREATE_SCHEME","powrprof/ACCESS_DC_POWER_SETTING_INDEX","powrprof/ACCESS_INDIVIDUAL_SETTING","powrprof/ACCESS_SCHEME","powrprof/ACCESS_SUBGROUP","powrprof/POWER_DATA_ACCESSOR","powrprof/PPOWER_DATA_ACCESSOR"]
old-location: base\power_data_accessor.htm
tech.root: base
ms.assetid: 4b3f8f89-2ade-4594-b055-b1873e74cda6
ms.date: 12/05/2018
ms.keywords: '*PPOWER_DATA_ACCESSOR, ACCESS_ACTIVE_SCHEME, ACCESS_AC_POWER_SETTING_INDEX, ACCESS_CREATE_SCHEME, ACCESS_DC_POWER_SETTING_INDEX, ACCESS_INDIVIDUAL_SETTING, ACCESS_SCHEME, ACCESS_SUBGROUP, POWER_DATA_ACCESSOR, POWER_DATA_ACCESSOR enumeration, PPOWER_DATA_ACCESSOR, PPOWER_DATA_ACCESSOR enumeration pointer, base.power_data_accessor, powrprof/ACCESS_ACTIVE_SCHEME, powrprof/ACCESS_AC_POWER_SETTING_INDEX, powrprof/ACCESS_CREATE_SCHEME, powrprof/ACCESS_DC_POWER_SETTING_INDEX, powrprof/ACCESS_INDIVIDUAL_SETTING, powrprof/ACCESS_SCHEME, powrprof/ACCESS_SUBGROUP, powrprof/POWER_DATA_ACCESSOR, powrprof/PPOWER_DATA_ACCESSOR'
req.header: powrprof.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: POWER_DATA_ACCESSOR, *PPOWER_DATA_ACCESSOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POWER_DATA_ACCESSOR
 - powrprof/_POWER_DATA_ACCESSOR
 - PPOWER_DATA_ACCESSOR
 - powrprof/PPOWER_DATA_ACCESSOR
 - POWER_DATA_ACCESSOR
 - powrprof/POWER_DATA_ACCESSOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PowrProf.h
api_name:
 - POWER_DATA_ACCESSOR
---

# POWER_DATA_ACCESSOR enumeration


## -description

Enumeration values used by <a href="/windows/desktop/api/powrprof/nf-powrprof-powerenumerate">PowerEnumerate</a> 
    and <a href="/windows/desktop/api/powrprof/nf-powrprof-powersettingaccesscheck">PowerSettingAccessCheck</a>.

## -enum-fields

### -field ACCESS_AC_POWER_SETTING_INDEX:0

Used with <a href="/windows/desktop/api/powrprof/nf-powrprof-powersettingaccesscheck">PowerSettingAccessCheck</a> to 
      check for group policy overrides for AC power settings.

### -field ACCESS_DC_POWER_SETTING_INDEX

Used with <a href="/windows/desktop/api/powrprof/nf-powrprof-powersettingaccesscheck">PowerSettingAccessCheck</a> to 
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
      <a href="/windows/desktop/api/powrprof/nf-powrprof-powerenumerate">PowerEnumerate</a> and with 
      <a href="/windows/desktop/api/powrprof/nf-powrprof-powersettingaccesscheck">PowerSettingAccessCheck</a> to check for 
      restricted access to specific power schemes.

### -field ACCESS_SUBGROUP

Used to enumerate subgroups with 
      <a href="/windows/desktop/api/powrprof/nf-powrprof-powerenumerate">PowerEnumerate</a>.

### -field ACCESS_INDIVIDUAL_SETTING

Used to enumerate individual power settings with 
      <a href="/windows/desktop/api/powrprof/nf-powrprof-powerenumerate">PowerEnumerate</a>.

### -field ACCESS_ACTIVE_SCHEME

Used with <a href="/windows/desktop/api/powrprof/nf-powrprof-powersettingaccesscheck">PowerSettingAccessCheck</a> to 
      check for group policy overrides for active power schemes.

### -field ACCESS_CREATE_SCHEME

Used with <a href="/windows/desktop/api/powrprof/nf-powrprof-powersettingaccesscheck">PowerSettingAccessCheck</a> to 
      check for restricted access for creating power schemes.

### -field ACCESS_AC_POWER_SETTING_MAX

### -field ACCESS_DC_POWER_SETTING_MAX

### -field ACCESS_AC_POWER_SETTING_MIN

### -field ACCESS_DC_POWER_SETTING_MIN

### -field ACCESS_PROFILE

### -field ACCESS_OVERLAY_SCHEME

### -field ACCESS_ACTIVE_OVERLAY_SCHEME

## -see-also

<a href="/windows/desktop/Power/power-management-enumeration-types">Power Management Enumeration Types</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-powerenumerate">PowerEnumerate</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-powersettingaccesscheck">PowerSettingAccessCheck</a>
