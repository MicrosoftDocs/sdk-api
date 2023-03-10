---
UID: NS:wsman._WSMAN_RESPONSE_DATA
title: WSMAN_RESPONSE_DATA (wsman.h)
description: Represents the output data received from a WSMan operation.
helpviewer_keywords: ["WSMAN_RESPONSE_DATA","WSMAN_RESPONSE_DATA union [Windows Remote Management]","winrm.wsman_response_data","wsman/WSMAN_RESPONSE_DATA"]
old-location: winrm\wsman_response_data.htm
tech.root: winrm
ms.assetid: 397AAE6C-8878-44B6-A025-4BC04514F6A7
ms.date: 12/05/2018
ms.keywords: WSMAN_RESPONSE_DATA, WSMAN_RESPONSE_DATA union [Windows Remote Management], winrm.wsman_response_data, wsman/WSMAN_RESPONSE_DATA
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: WSMAN_RESPONSE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSMAN_RESPONSE_DATA
 - wsman/_WSMAN_RESPONSE_DATA
 - WSMAN_RESPONSE_DATA
 - wsman/WSMAN_RESPONSE_DATA
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
 - WSMAN_RESPONSE_DATA
---

# WSMAN_RESPONSE_DATA structure


## -description

Represents the output data received from a <a href="/windows/desktop/WinRM/wsman">WSMan</a> operation.

## -struct-fields

### -field receiveData

Represents the output data received from a <a href="/windows/desktop/api/wsman/nf-wsman-wsmanreceiveshelloutput">WSManReceiveShellOutput</a> method.

### -field connectData

Represents the output data received from a <a href="/windows/desktop/api/wsman/nf-wsman-wsmanconnectshell">WSManConnectShell</a> or <a href="/windows/desktop/api/wsman/nf-wsman-wsmanconnectshellcommand">WSManConnectShellCommand</a> method.

### -field createData