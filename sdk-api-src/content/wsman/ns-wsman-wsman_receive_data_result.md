---
UID: NS:wsman._WSMAN_RECEIVE_DATA_RESULT
title: WSMAN_RECEIVE_DATA_RESULT (wsman.h)
description: Represents the output data received from a WSManReceiveShellOutput method.
helpviewer_keywords: ["WSMAN_RECEIVE_DATA_RESULT","WSMAN_RECEIVE_DATA_RESULT structure [Windows Remote Management]","winrm.wsman_receive_data_result","wsman/WSMAN_RECEIVE_DATA_RESULT"]
old-location: winrm\wsman_receive_data_result.htm
tech.root: winrm
ms.assetid: e649a4f0-37ae-40cb-9245-e1b792034c8a
ms.date: 12/05/2018
ms.keywords: WSMAN_RECEIVE_DATA_RESULT, WSMAN_RECEIVE_DATA_RESULT structure [Windows Remote Management], winrm.wsman_receive_data_result, wsman/WSMAN_RECEIVE_DATA_RESULT
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
req.typenames: WSMAN_RECEIVE_DATA_RESULT
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_RECEIVE_DATA_RESULT
 - wsman/_WSMAN_RECEIVE_DATA_RESULT
 - WSMAN_RECEIVE_DATA_RESULT
 - wsman/WSMAN_RECEIVE_DATA_RESULT
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
 - WSMAN_RECEIVE_DATA_RESULT
---

# WSMAN_RECEIVE_DATA_RESULT structure


## -description

Represents the output data received from a <a href="/windows/desktop/api/wsman/nf-wsman-wsmanreceiveshelloutput">WSManReceiveShellOutput</a> method.

## -struct-fields

### -field streamId

Represents the <b>streamId</b> for which <b>streamData</b> is defined.

### -field streamData

Represents the data associated with <b>streamId</b>. The data can be stream text, binary content, or XML. For more information about the possible data, see <a href="/windows/desktop/api/wsman/ns-wsman-wsman_data">WSMAN_DATA</a>.

### -field commandState

Specifies the status of the command. If this member is set to <b>WSMAN_COMMAND_STATE_DONE</b>, the command should be immediately closed.

### -field exitCode

Defines the exit code of the command. This value is relevant only if the <b>commandState</b> member is set to <b>WSMAN_COMMAND_STATE_DONE</b>.