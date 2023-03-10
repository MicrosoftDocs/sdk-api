---
UID: NS:ndattrib.tagUiInfo
title: UiInfo (ndattrib.h)
description: The UiInfo structure is used to display repair messages to the user.
helpviewer_keywords: ["*PUiInfo","UiInfo","UiInfo structure [NDF]","UiInfo","*PUiInfo","UiInfo","*PUiInfo structure [NDF]","ndattrib/UiInfo","ndf.uiinfo"]
old-location: ndf\uiinfo.htm
tech.root: NDF
ms.assetid: 62d3c908-8fc4-4bd9-94ac-94dfcf8db395
ms.date: 12/05/2018
ms.keywords: '*PUiInfo, UiInfo, UiInfo structure [NDF], UiInfo,*PUiInfo, UiInfo,*PUiInfo structure [NDF], ndattrib/UiInfo, ndf.uiinfo'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UiInfo, *PUiInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUiInfo
 - ndattrib/tagUiInfo
 - PUiInfo
 - ndattrib/PUiInfo
 - UiInfo
 - ndattrib/UiInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndattrib.h
api_name:
 - UiInfo, *PUiInfo
---

# UiInfo structure


## -description

The <b>UiInfo</b> structure is used to display repair messages to the user.

## -struct-fields

### -field type

Type: <b><a href="/windows/win32/api/ndattrib/ne-ndattrib-ui_info_type">UI_INFO_TYPE</a></b>

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

<a href="/windows/desktop/NDF/freeuiinfo">FreeUiInfo</a>



<a href="/windows/win32/api/ndattrib/ne-ndattrib-ui_info_type">UI_INFO_TYPE</a>