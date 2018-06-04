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

# tagOFFLINEFILES_SETTING_VALUE_TYPE enumeration


## -description


Identifies the data type returned by the <a href="https://msdn.microsoft.com/2b5567bf-a7c6-40b3-ac16-9da805ddb3b3">IOfflineFilesSetting::GetValueType</a> method.


## -enum-fields




### -field OFFLINEFILES_SETTING_VALUE_UI4

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




<a href="https://msdn.microsoft.com/2b5567bf-a7c6-40b3-ac16-9da805ddb3b3">IOfflineFilesSetting::GetValueType</a>
 

 

