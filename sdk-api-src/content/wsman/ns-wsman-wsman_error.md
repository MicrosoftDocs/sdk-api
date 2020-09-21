---
UID: NS:wsman._WSMAN_ERROR
title: WSMAN_ERROR (wsman.h)
description: Contains error information that is returned by a Windows Remote Management (WinRM) client.
helpviewer_keywords: ["WSMAN_ERROR","WSMAN_ERROR structure [Windows Remote Management]","winrm.wsman_error_struct","wsman/WSMAN_ERROR"]
old-location: winrm\wsman_error_struct.htm
tech.root: winrm
ms.assetid: 6705b560-9c72-4cb9-a290-f7c65cd470b2
ms.date: 12/05/2018
ms.keywords: WSMAN_ERROR, WSMAN_ERROR structure [Windows Remote Management], winrm.wsman_error_struct, wsman/WSMAN_ERROR
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
req.typenames: WSMAN_ERROR
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_ERROR
 - wsman/_WSMAN_ERROR
 - WSMAN_ERROR
 - wsman/WSMAN_ERROR
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
 - WSMAN_ERROR
---

# WSMAN_ERROR structure


## -description

Contains error information that is returned by a Windows Remote Management (WinRM) client. The <a href="/windows/desktop/WinRM/wsman-error">WSMAN_ERROR</a> structure is used by all callbacks to return error information and is valid only for the callback.

## -struct-fields

### -field code

Specifies an error code. This error can be a general error code that is defined in winerror.h or a WinRM-specific error code.

### -field errorDetail

Specifies extended error information that relates to a failed call. This field contains the fault detail text if it is present in the fault. If there is no fault detail, this field contains the fault reason text. This field can be set to <b>NULL</b>.

### -field language

Specifies the language for the error description. This field can be set to <b>NULL</b>.  For more information about the language format, see the    RFC 3066 specification from the Internet Engineering Task Force at <a href="https://www.ietf.org/rfc/rfc3066.txt">http://www.ietf.org/rfc/rfc3066.txt</a>.

### -field machineName

Specifies the name of the computer. This field can be set to <b>NULL</b>.

### -field pluginName

Specifies the name of the plug-in that generated the error. This field can be set to <b>NULL</b>.