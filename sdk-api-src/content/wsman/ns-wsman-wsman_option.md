---
UID: NS:wsman._WSMAN_OPTION
title: WSMAN_OPTION (wsman.h)
description: Represents a specific option name and value pair.
helpviewer_keywords: ["WSMAN_OPTION","WSMAN_OPTION structure [Windows Remote Management]","winrm.wsman_option","wsman/WSMAN_OPTION"]
old-location: winrm\wsman_option.htm
tech.root: winrm
ms.assetid: 9ebb9b21-1418-476d-a7a2-395c77f26dc9
ms.date: 12/05/2018
ms.keywords: WSMAN_OPTION, WSMAN_OPTION structure [Windows Remote Management], winrm.wsman_option, wsman/WSMAN_OPTION
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
req.typenames: WSMAN_OPTION
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_OPTION
 - wsman/_WSMAN_OPTION
 - WSMAN_OPTION
 - wsman/WSMAN_OPTION
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
 - WSMAN_OPTION
---

# WSMAN_OPTION structure


## -description

Represents a specific option name and value pair.  An option that is not understood and has a <b>mustComply</b> value of <b>TRUE</b> should result in the plug-in operation failing the request with an error.

## -struct-fields

### -field name

Specifies the name of the option.

### -field value

Specifies the value of the option.

### -field mustComply

Specifies whether the option must be understood and complied with.  If this value is <b>TRUE</b>, the plug-in must understand and adhere to the meaning of the option; otherwise, the plug-in must return an error.  If this is <b>FALSE</b>, the plug-in should ignore the option if it is not understood.

