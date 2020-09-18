---
UID: NS:wsman._WSMAN_ENVIRONMENT_VARIABLE_SET
title: WSMAN_ENVIRONMENT_VARIABLE_SET (wsman.h)
description: Defines an array of environment variables.
helpviewer_keywords: ["WSMAN_ENVIRONMENT_VARIABLE_SET","WSMAN_ENVIRONMENT_VARIABLE_SET structure [Windows Remote Management]","winrm.wsman_environment_variable_set","wsman/WSMAN_ENVIRONMENT_VARIABLE_SET"]
old-location: winrm\wsman_environment_variable_set.htm
tech.root: winrm
ms.assetid: 3d9b4374-241f-489e-946a-9c180d77de3b
ms.date: 12/05/2018
ms.keywords: WSMAN_ENVIRONMENT_VARIABLE_SET, WSMAN_ENVIRONMENT_VARIABLE_SET structure [Windows Remote Management], winrm.wsman_environment_variable_set, wsman/WSMAN_ENVIRONMENT_VARIABLE_SET
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
req.typenames: WSMAN_ENVIRONMENT_VARIABLE_SET
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_ENVIRONMENT_VARIABLE_SET
 - wsman/_WSMAN_ENVIRONMENT_VARIABLE_SET
 - WSMAN_ENVIRONMENT_VARIABLE_SET
 - wsman/WSMAN_ENVIRONMENT_VARIABLE_SET
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
 - WSMAN_ENVIRONMENT_VARIABLE_SET
---

# WSMAN_ENVIRONMENT_VARIABLE_SET structure


## -description

Defines an array of environment variables.

## -struct-fields

### -field varsCount

Specifies the number of environment variables contained within the <b>vars</b> array.

### -field vars

Defines an array of environment variables. Each element of the array is of type <a href="/windows/desktop/api/wsman/ns-wsman-wsman_environment_variable">WSMAN_ENVIRONMENT_VARIABLE</a>.