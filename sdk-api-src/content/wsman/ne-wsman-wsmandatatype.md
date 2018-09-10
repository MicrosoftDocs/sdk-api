---
UID: NE:wsman.WSManDataType
title: WSManDataType
author: windows-sdk-content
description: Specifies the current data type of the union in the WSMAN_DATA structure.
old-location: winrm\wsmandatatype.htm
tech.root: WinRM
ms.assetid: c5f58532-cd84-4440-909d-7d3dba0cff50
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WSMAN_DATA_NONE, WSMAN_DATA_TYPE_BINARY, WSMAN_DATA_TYPE_DWORD, WSMAN_DATA_TYPE_TEXT, WSManDataType, WSManDataType enumeration [Windows Remote Management], winrm.wsmandatatype, wsman/WSMAN_DATA_NONE, wsman/WSMAN_DATA_TYPE_BINARY, wsman/WSMAN_DATA_TYPE_DWORD, wsman/WSMAN_DATA_TYPE_TEXT, wsman/WSManDataType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: WSManDataType
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
---

# WSManDataType enumeration


## -description


Specifies the current data type of the union in the <a href="https://msdn.microsoft.com/4ff574d4-04b0-47c3-808f-867d6815bffc">WSMAN_DATA</a> structure.


## -enum-fields




### -field WSMAN_DATA_NONE

The structure is not valid yet.


### -field WSMAN_DATA_TYPE_TEXT

The structure contains text.


### -field WSMAN_DATA_TYPE_BINARY

The structure contains binary data.


### -field WSMAN_DATA_TYPE_DWORD

The structure contains a DWORD integer.

