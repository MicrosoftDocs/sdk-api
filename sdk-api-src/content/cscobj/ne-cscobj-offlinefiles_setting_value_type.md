---
UID: NE:cscobj.tagOFFLINEFILES_SETTING_VALUE_TYPE
title: OFFLINEFILES_SETTING_VALUE_TYPE (cscobj.h)
description: Identifies the data type returned by the IOfflineFilesSetting::GetValueType method.
helpviewer_keywords: ["OFFLINEFILES_SETTING_VALUE_2DIM_ARRAY_BSTR_BSTR","OFFLINEFILES_SETTING_VALUE_2DIM_ARRAY_BSTR_UI4","OFFLINEFILES_SETTING_VALUE_BSTR","OFFLINEFILES_SETTING_VALUE_BSTR_DBLNULTERM","OFFLINEFILES_SETTING_VALUE_TYPE","OFFLINEFILES_SETTING_VALUE_TYPE enumeration [Offline Files]","OFFLINEFILES_SETTING_VALUE_UI4","cscobj/OFFLINEFILES_SETTING_VALUE_2DIM_ARRAY_BSTR_BSTR","cscobj/OFFLINEFILES_SETTING_VALUE_2DIM_ARRAY_BSTR_UI4","cscobj/OFFLINEFILES_SETTING_VALUE_BSTR","cscobj/OFFLINEFILES_SETTING_VALUE_BSTR_DBLNULTERM","cscobj/OFFLINEFILES_SETTING_VALUE_TYPE","cscobj/OFFLINEFILES_SETTING_VALUE_UI4","of.offlinefiles_setting_value_type"]
old-location: of\offlinefiles_setting_value_type.htm
tech.root: of
ms.assetid: 37569197-efd3-4e4e-953a-3bbd2cb07d5a
ms.date: 12/05/2018
ms.keywords: OFFLINEFILES_SETTING_VALUE_2DIM_ARRAY_BSTR_BSTR, OFFLINEFILES_SETTING_VALUE_2DIM_ARRAY_BSTR_UI4, OFFLINEFILES_SETTING_VALUE_BSTR, OFFLINEFILES_SETTING_VALUE_BSTR_DBLNULTERM, OFFLINEFILES_SETTING_VALUE_TYPE, OFFLINEFILES_SETTING_VALUE_TYPE enumeration [Offline Files], OFFLINEFILES_SETTING_VALUE_UI4, cscobj/OFFLINEFILES_SETTING_VALUE_2DIM_ARRAY_BSTR_BSTR, cscobj/OFFLINEFILES_SETTING_VALUE_2DIM_ARRAY_BSTR_UI4, cscobj/OFFLINEFILES_SETTING_VALUE_BSTR, cscobj/OFFLINEFILES_SETTING_VALUE_BSTR_DBLNULTERM, cscobj/OFFLINEFILES_SETTING_VALUE_TYPE, cscobj/OFFLINEFILES_SETTING_VALUE_UI4, of.offlinefiles_setting_value_type
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: OFFLINEFILES_SETTING_VALUE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOFFLINEFILES_SETTING_VALUE_TYPE
 - cscobj/tagOFFLINEFILES_SETTING_VALUE_TYPE
 - OFFLINEFILES_SETTING_VALUE_TYPE
 - cscobj/OFFLINEFILES_SETTING_VALUE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CscObj.h
api_name:
 - OFFLINEFILES_SETTING_VALUE_TYPE
---

# OFFLINEFILES_SETTING_VALUE_TYPE enumeration


## -description

Identifies the data type returned by the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessetting-getvaluetype">IOfflineFilesSetting::GetValueType</a> method.

## -enum-fields

### -field OFFLINEFILES_SETTING_VALUE_UI4:0

A single VT_UI4 value. Used to represent single REG_DWORD values. REG_DWORD is by far the most common type of setting value.

### -field OFFLINEFILES_SETTING_VALUE_BSTR

A single VT_BSTR value.  Used to represent single REG_SZ and REG_EXPAND_SZ values.

### -field OFFLINEFILES_SETTING_VALUE_BSTR_DBLNULTERM

A single VT_BSTR value.  The string is a double-null-terminated string containing multiple null-terminated substrings. Used to represent single REG_MULTI_SZ values.

### -field OFFLINEFILES_SETTING_VALUE_2DIM_ARRAY_BSTR_UI4

A 2-dimensional array.  Each row is a <i>name,value</i> pair. Used to represent a set of REG_DWORD values under a registry key of the same name as the setting.  Typically, the value names contain UNC paths and the values contain a parameter associated with each UNC path. Column 0 is the value name expressed as VT_BSTR. Column 1 is the VT_UI4 value.

### -field OFFLINEFILES_SETTING_VALUE_2DIM_ARRAY_BSTR_BSTR

A 2-dimensional array.  Each row is a <i>name,value</i> pair. Used to represent a set of BSTR values under a registry key of the same name as the setting.  Typically, the value names contain UNC paths and the values contain a parameter associated with each UNC path. Column 0 is the value name expressed as VT_BSTR. Column 1 is the VT_BSTR value.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessetting-getvaluetype">IOfflineFilesSetting::GetValueType</a>
