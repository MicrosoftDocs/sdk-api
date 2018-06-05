---
UID: NS:ndattrib.tagUiInfo
title: tagUiInfo
author: windows-sdk-content
description: The UiInfo structure is used to display repair messages to the user.
old-location: ndf\uiinfo.htm
old-project: NDF
ms.assetid: 62d3c908-8fc4-4bd9-94ac-94dfcf8db395
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*PUiInfo, UiInfo, UiInfo structure [NDF], UiInfo,*PUiInfo, UiInfo,*PUiInfo structure [NDF], ndattrib/UiInfo, ndf.uiinfo, tagUiInfo"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ndattrib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ndattrib.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UiInfo, *PUiInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ndattrib.h
api_name:
-	UiInfo, *PUiInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

