---
UID: NS:wsman._WSMAN_DATA_BINARY
title: WSMAN_DATA_BINARY (wsman.h)
description: Holds binary data for use with various Windows Remote Management functions.
helpviewer_keywords: ["WSMAN_DATA_BINARY","WSMAN_DATA_BINARY structure [Windows Remote Management]","winrm.wsman_data_binary","wsman/WSMAN_DATA_BINARY"]
old-location: winrm\wsman_data_binary.htm
tech.root: winrm
ms.assetid: 35beedc3-30c6-4e04-bc27-bb9eb21256fe
ms.date: 12/05/2018
ms.keywords: WSMAN_DATA_BINARY, WSMAN_DATA_BINARY structure [Windows Remote Management], winrm.wsman_data_binary, wsman/WSMAN_DATA_BINARY
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
req.typenames: WSMAN_DATA_BINARY
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_DATA_BINARY
 - wsman/_WSMAN_DATA_BINARY
 - WSMAN_DATA_BINARY
 - wsman/WSMAN_DATA_BINARY
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
 - WSMAN_DATA_BINARY
---

# WSMAN_DATA_BINARY structure


## -description

A <a href="/windows/desktop/api/wsman/ns-wsman-wsman_data">WSMAN_DATA</a> structure component that holds binary data for use with various Windows Remote Management functions.

## -struct-fields

### -field dataLength

Represents the number of BYTEs stored in the data field.

### -field data

Specifies the storage location for the binary data.