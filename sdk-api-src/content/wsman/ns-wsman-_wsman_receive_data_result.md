---
UID: NS:wsman._WSMAN_RECEIVE_DATA_RESULT
title: "_WSMAN_RECEIVE_DATA_RESULT"
author: windows-sdk-content
description: Represents the output data received from a WSManReceiveShellOutput method.
old-location: winrm\wsman_receive_data_result.htm
tech.root: WinRM
ms.assetid: e649a4f0-37ae-40cb-9245-e1b792034c8a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WSMAN_RECEIVE_DATA_RESULT, WSMAN_RECEIVE_DATA_RESULT structure [Windows Remote Management], _WSMAN_RECEIVE_DATA_RESULT, winrm.wsman_receive_data_result, wsman/WSMAN_RECEIVE_DATA_RESULT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - WSMAN_RECEIVE_DATA_RESULT
product: Windows
targetos: Windows
req.typenames: WSMAN_RECEIVE_DATA_RESULT
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
---

# _WSMAN_RECEIVE_DATA_RESULT structure


## -description


Represents the output data received from a <a href="https://msdn.microsoft.com/cc64f212-9897-4a58-b3f1-bc2093f593ba">WSManReceiveShellOutput</a> method.




## -struct-fields




### -field streamId

Represents the <b>streamId</b> for which <b>streamData</b> is defined.


### -field streamData

Represents the data associated with <b>streamId</b>. The data can be stream text, binary content, or XML. For more information about the possible data, see <a href="https://msdn.microsoft.com/4ff574d4-04b0-47c3-808f-867d6815bffc">WSMAN_DATA</a>.


### -field commandState

Specifies the status of the command. If this member is set to <b>WSMAN_COMMAND_STATE_DONE</b>, the command should be immediately closed.


### -field exitCode

Defines the exit code of the command. This value is relevant only if the <b>commandState</b> member is set to <b>WSMAN_COMMAND_STATE_DONE</b>.

