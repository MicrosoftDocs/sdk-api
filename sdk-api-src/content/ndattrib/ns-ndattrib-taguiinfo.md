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

# tagUiInfo structure


## -description


The <b>UiInfo</b> structure is used to display repair messages to the user.


## -struct-fields




### -field type

Type: <b><a href="https://msdn.microsoft.com/819ab594-860b-42a0-be6e-bab0e669c200">UI_INFO_TYPE</a></b>

The type of user interface (UI) to use. This can be one of the values shown in the following members.


### -field pwzNull

Type: <b>LPWSTR</b>

No additional UI is required. Used when <b>type</b> is set to UIT_NONE.


### -field ShellInfo

Type: <b>ShellCommandInfo</b>

Execute a shell command.  Used when <b>type</b> is set to UIT_SHELL_COMMAND.


### -field pwzHelpUrl

Type: <b>LPWSTR</b>

Launches a help pane. Used when <b>type</b> is set to UIT_HELP_PANE.


### -field pwzDui

Type: <b>LPWSTR</b>

Use a direct user interface. Used when <b>type</b> is set to UIT_DUI.


## -see-also




<a href="https://msdn.microsoft.com/41d923fd-2fb3-406e-a5cf-f3ba475685f6">FreeUiInfo</a>



<a href="https://msdn.microsoft.com/819ab594-860b-42a0-be6e-bab0e669c200">UI_INFO_TYPE</a>
 

 

