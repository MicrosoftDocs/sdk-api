---
UID: NE:wsman.WSManDataType
title: WSManDataType (wsman.h)
description: Specifies the current data type of the union in the WSMAN_DATA structure.helpviewer_keywords: ["WSMAN_DATA_NONE","WSMAN_DATA_TYPE_BINARY","WSMAN_DATA_TYPE_DWORD","WSMAN_DATA_TYPE_TEXT","WSManDataType","WSManDataType enumeration [Windows Remote Management]","winrm.wsmandatatype","wsman/WSMAN_DATA_NONE","wsman/WSMAN_DATA_TYPE_BINARY","wsman/WSMAN_DATA_TYPE_DWORD","wsman/WSMAN_DATA_TYPE_TEXT","wsman/WSManDataType"]
old-location: winrm\wsmandatatype.htm
tech.root: winrm
ms.assetid: c5f58532-cd84-4440-909d-7d3dba0cff50
ms.date: 12/05/2018
ms.keywords: WSMAN_DATA_NONE, WSMAN_DATA_TYPE_BINARY, WSMAN_DATA_TYPE_DWORD, WSMAN_DATA_TYPE_TEXT, WSManDataType, WSManDataType enumeration [Windows Remote Management], winrm.wsmandatatype, wsman/WSMAN_DATA_NONE, wsman/WSMAN_DATA_TYPE_BINARY, wsman/WSMAN_DATA_TYPE_DWORD, wsman/WSMAN_DATA_TYPE_TEXT, wsman/WSManDataType
f1_keywords:
- wsman/WSManDataType
dev_langs:
- c++
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
- Wsman.h
api_name:
- WSManDataType
targetos: Windows
req.typenames: WSManDataType
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
---

# WSManDataType enumeration


## -description


Specifies the current data type of the union in the <a href="https://docs.microsoft.com/windows/desktop/api/wsman/ns-wsman-wsman_data">WSMAN_DATA</a> structure.


## -enum-fields




### -field WSMAN_DATA_NONE

The structure is not valid yet.


### -field WSMAN_DATA_TYPE_TEXT

The structure contains text.


### -field WSMAN_DATA_TYPE_BINARY

The structure contains binary data.


### -field WSMAN_DATA_TYPE_DWORD

The structure contains a DWORD integer.

