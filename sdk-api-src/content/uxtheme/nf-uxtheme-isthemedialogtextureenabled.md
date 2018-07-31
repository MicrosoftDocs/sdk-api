---
UID: NF:uxtheme.IsThemeDialogTextureEnabled
title: IsThemeDialogTextureEnabled function
author: windows-sdk-content
description: Reports whether a specified dialog window supports background texturing.
old-location: controls\IsThemeDialogTextureEnabled.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\isthemedialogtextureenabled.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IsThemeDialogTextureEnabled, IsThemeDialogTextureEnabled function [Windows Controls], controls.IsThemeDialogTextureEnabled, controls.inet_IsThemeDialogTextureEnabled, inet_IsThemeDialogTextureEnabled, inet_IsThemeDialogTextureEnabled_cpp, uxtheme/IsThemeDialogTextureEnabled
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BP_BUFFERFORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - IsThemeDialogTextureEnabled
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll (version 1.0 or later)
req.irql: 
req.product: Windows UI
---

# IsThemeDialogTextureEnabled function


## -description


Reports whether a specified dialog window supports background texturing.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

<b>HWND</b> value that specifies a dialog window. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Background texturing is supported on the dialog window specified by the <i>hwnd</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Background texturing is not supported on the dialog window specified by the <i>hwnd</i> parameter.

</td>
</tr>
</table>
 



