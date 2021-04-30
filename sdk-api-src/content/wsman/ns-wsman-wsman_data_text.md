---
UID: NS:wsman._WSMAN_DATA_TEXT
title: WSMAN_DATA_TEXT (wsman.h)
description: Holds textual data for use with various Windows Remote Management functions.
helpviewer_keywords: ["WSMAN_DATA_TEXT","WSMAN_DATA_TEXT structure [Windows Remote Management]","winrm.wsman_data_text","wsman/WSMAN_DATA_TEXT"]
old-location: winrm\wsman_data_text.htm
tech.root: winrm
ms.assetid: 463dcc6a-2a56-42a9-a778-7a634e5f977c
ms.date: 12/05/2018
ms.keywords: WSMAN_DATA_TEXT, WSMAN_DATA_TEXT structure [Windows Remote Management], winrm.wsman_data_text, wsman/WSMAN_DATA_TEXT
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
targetos: Windows
req.typenames: WSMAN_DATA_TEXT
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_DATA_TEXT
 - wsman/_WSMAN_DATA_TEXT
 - WSMAN_DATA_TEXT
 - wsman/WSMAN_DATA_TEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_DATA_TEXT
---

# WSMAN_DATA_TEXT structure


## -description

A <a href="/windows/desktop/api/wsman/ns-wsman-wsman_data">WSMAN_DATA</a> structure component that holds textual data for use with various Windows Remote Management functions.

## -struct-fields

### -field bufferLength

Specifies the number of UNICODE characters stored in the buffer.

### -field buffer

Specifies the storage location for the textual data.