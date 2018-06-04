---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

