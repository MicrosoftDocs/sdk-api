---
UID: NS:wsman._WSMAN_OPERATION_INFO
title: WSMAN_OPERATION_INFO (wsman.h)
description: Represents a specific resource endpoint for which the plug-in must perform the request.
helpviewer_keywords: ["WSMAN_OPERATION_INFO","WSMAN_OPERATION_INFO structure [Windows Remote Management]","winrm.wsman_operation_info","wsman/WSMAN_OPERATION_INFO"]
old-location: winrm\wsman_operation_info.htm
tech.root: winrm
ms.assetid: a73029c6-d4e7-4cb3-ad0a-b71baffdbeb6
ms.date: 12/05/2018
ms.keywords: WSMAN_OPERATION_INFO, WSMAN_OPERATION_INFO structure [Windows Remote Management], winrm.wsman_operation_info, wsman/WSMAN_OPERATION_INFO
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
req.typenames: WSMAN_OPERATION_INFO
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_OPERATION_INFO
 - wsman/_WSMAN_OPERATION_INFO
 - WSMAN_OPERATION_INFO
 - wsman/WSMAN_OPERATION_INFO
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
 - WSMAN_OPERATION_INFO
---

# WSMAN_OPERATION_INFO structure


## -description

Represents a specific resource endpoint for which the plug-in must perform the request.

## -struct-fields

### -field fragment

A <a href="/windows/desktop/api/wsman/ns-wsman-wsman_fragment">WSMAN_FRAGMENT</a> structure that specifies the subset of data to be used for the operation. This parameter is reserved for future use and is ignored on receipt.

### -field filter

A <a href="/windows/desktop/api/wsman/ns-wsman-wsman_filter">WSMAN_FILTER</a> structure that specifies the filtering that is used for the operation. This parameter is reserved for future use and is ignored on receipt.

### -field selectorSet

A <a href="/windows/desktop/api/wsman/ns-wsman-wsman_selector_set">WSMAN_SELECTOR_SET</a> structure that identifies the specific resource to use for the request.

### -field optionSet

A <a href="/windows/desktop/api/wsman/ns-wsman-wsman_option_set">WSMAN_OPTION_SET</a> structure that specifies the set of options for the request.

### -field reserved

### -field version