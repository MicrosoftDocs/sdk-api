---
UID: NE:wbemcli.tag_WMI_OBJ_TEXT
title: WMI_OBJ_TEXT (wbemcli.h)
description: Defines the valid object text formats to be used by SWbemObjectEx.GetText_.
helpviewer_keywords: ["WMI_OBJ_TEXT","WMI_OBJ_TEXT enumeration [Windows Management Instrumentation]","WMI_OBJ_TEXT_CIM_DTD_2_0","WMI_OBJ_TEXT_LAST","WMI_OBJ_TEXT_WMI_DTD_2_0","WMI_OBJ_TEXT_WMI_EXT1","WMI_OBJ_TEXT_WMI_EXT10","WMI_OBJ_TEXT_WMI_EXT2","WMI_OBJ_TEXT_WMI_EXT3","WMI_OBJ_TEXT_WMI_EXT4","WMI_OBJ_TEXT_WMI_EXT5","WMI_OBJ_TEXT_WMI_EXT6","WMI_OBJ_TEXT_WMI_EXT7","WMI_OBJ_TEXT_WMI_EXT8","WMI_OBJ_TEXT_WMI_EXT9","wbemcli/WMI_OBJ_TEXT","wbemcli/WMI_OBJ_TEXT_CIM_DTD_2_0","wbemcli/WMI_OBJ_TEXT_LAST","wbemcli/WMI_OBJ_TEXT_WMI_DTD_2_0","wbemcli/WMI_OBJ_TEXT_WMI_EXT1","wbemcli/WMI_OBJ_TEXT_WMI_EXT10","wbemcli/WMI_OBJ_TEXT_WMI_EXT2","wbemcli/WMI_OBJ_TEXT_WMI_EXT3","wbemcli/WMI_OBJ_TEXT_WMI_EXT4","wbemcli/WMI_OBJ_TEXT_WMI_EXT5","wbemcli/WMI_OBJ_TEXT_WMI_EXT6","wbemcli/WMI_OBJ_TEXT_WMI_EXT7","wbemcli/WMI_OBJ_TEXT_WMI_EXT8","wbemcli/WMI_OBJ_TEXT_WMI_EXT9","wmi.wmi_obj_text"]
old-location: wmi\wmi_obj_text.htm
tech.root: wmi
ms.assetid: 18970FA8-F42E-4F3D-9D79-37B841814AF8
ms.date: 12/05/2018
ms.keywords: WMI_OBJ_TEXT, WMI_OBJ_TEXT enumeration [Windows Management Instrumentation], WMI_OBJ_TEXT_CIM_DTD_2_0, WMI_OBJ_TEXT_LAST, WMI_OBJ_TEXT_WMI_DTD_2_0, WMI_OBJ_TEXT_WMI_EXT1, WMI_OBJ_TEXT_WMI_EXT10, WMI_OBJ_TEXT_WMI_EXT2, WMI_OBJ_TEXT_WMI_EXT3, WMI_OBJ_TEXT_WMI_EXT4, WMI_OBJ_TEXT_WMI_EXT5, WMI_OBJ_TEXT_WMI_EXT6, WMI_OBJ_TEXT_WMI_EXT7, WMI_OBJ_TEXT_WMI_EXT8, WMI_OBJ_TEXT_WMI_EXT9, wbemcli/WMI_OBJ_TEXT, wbemcli/WMI_OBJ_TEXT_CIM_DTD_2_0, wbemcli/WMI_OBJ_TEXT_LAST, wbemcli/WMI_OBJ_TEXT_WMI_DTD_2_0, wbemcli/WMI_OBJ_TEXT_WMI_EXT1, wbemcli/WMI_OBJ_TEXT_WMI_EXT10, wbemcli/WMI_OBJ_TEXT_WMI_EXT2, wbemcli/WMI_OBJ_TEXT_WMI_EXT3, wbemcli/WMI_OBJ_TEXT_WMI_EXT4, wbemcli/WMI_OBJ_TEXT_WMI_EXT5, wbemcli/WMI_OBJ_TEXT_WMI_EXT6, wbemcli/WMI_OBJ_TEXT_WMI_EXT7, wbemcli/WMI_OBJ_TEXT_WMI_EXT8, wbemcli/WMI_OBJ_TEXT_WMI_EXT9, wmi.wmi_obj_text
req.header: wbemcli.h
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
req.typenames: WMI_OBJ_TEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_WMI_OBJ_TEXT
 - wbemcli/tag_WMI_OBJ_TEXT
 - WMI_OBJ_TEXT
 - wbemcli/WMI_OBJ_TEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemcli.h
api_name:
 - WMI_OBJ_TEXT
---

# WMI_OBJ_TEXT enumeration


## -description

Defines the valid object text formats to be used by 
<a href="/windows/desktop/WmiSdk/swbemobjectex-gettext-">SWbemObjectEx.GetText_</a>.

## -enum-fields

### -field WMI_OBJ_TEXT_CIM_DTD_2_0:1

XML format conforming to the DMTF (Distributed Management Task Force) CIM document type definition (DTD) version 2.0.

### -field WMI_OBJ_TEXT_WMI_DTD_2_0:2

XML format as defined by the extended WMI version of DMTF CIM DTD version 2.0. Using this value enables WMI-specific extensions, such as embedded objects or scope.

### -field WMI_OBJ_TEXT_WMI_EXT1:3

Deprecated. Do not use.

### -field WMI_OBJ_TEXT_WMI_EXT2:4

Deprecated. Do not use.

### -field WMI_OBJ_TEXT_WMI_EXT3:5

Deprecated. Do not use.

### -field WMI_OBJ_TEXT_WMI_EXT4:6

Deprecated. Do not use.

### -field WMI_OBJ_TEXT_WMI_EXT5:7

Deprecated. Do not use.

### -field WMI_OBJ_TEXT_WMI_EXT6:8

Deprecated. Do not use.

### -field WMI_OBJ_TEXT_WMI_EXT7:9

Deprecated. Do not use.

### -field WMI_OBJ_TEXT_WMI_EXT8:10

Deprecated. Do not use.

### -field WMI_OBJ_TEXT_WMI_EXT9:11

Deprecated. Do not use.

### -field WMI_OBJ_TEXT_WMI_EXT10:12

Deprecated. Do not use.

### -field WMI_OBJ_TEXT_LAST:13

Deprecated. Do not use.
