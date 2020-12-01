---
UID: NS:wsman._WSMAN_ENVIRONMENT_VARIABLE
title: WSMAN_ENVIRONMENT_VARIABLE (wsman.h)
description: Defines an individual environment variable by using a name and value pair.
helpviewer_keywords: ["WSMAN_ENVIRONMENT_VARIABLE","WSMAN_ENVIRONMENT_VARIABLE structure [Windows Remote Management]","winrm.wsman_environment_variable","wsman/WSMAN_ENVIRONMENT_VARIABLE"]
old-location: winrm\wsman_environment_variable.htm
tech.root: winrm
ms.assetid: 0bf58de5-0c0b-4dc2-ba8b-c75e8201adc8
ms.date: 12/05/2018
ms.keywords: WSMAN_ENVIRONMENT_VARIABLE, WSMAN_ENVIRONMENT_VARIABLE structure [Windows Remote Management], winrm.wsman_environment_variable, wsman/WSMAN_ENVIRONMENT_VARIABLE
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
req.typenames: WSMAN_ENVIRONMENT_VARIABLE
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_ENVIRONMENT_VARIABLE
 - wsman/_WSMAN_ENVIRONMENT_VARIABLE
 - WSMAN_ENVIRONMENT_VARIABLE
 - wsman/WSMAN_ENVIRONMENT_VARIABLE
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
 - WSMAN_ENVIRONMENT_VARIABLE
---

# WSMAN_ENVIRONMENT_VARIABLE structure


## -description

Defines an individual environment variable by using a name and value pair. This structure  is used by the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> method. The representation of the <b>value</b> variable is shell specific. The client and server must  agree on the format of the <b>value</b> variable.

## -struct-fields

### -field name

Defines the environment variable name. This parameter cannot be <b>NULL</b>.

### -field value

Defines the environment variable value. <b>NULL</b> or empty string values are permitted.