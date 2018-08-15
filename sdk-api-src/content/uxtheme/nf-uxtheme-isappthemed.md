---
UID: NF:uxtheme.IsAppThemed
title: IsAppThemed function
author: windows-sdk-content
description: Reports whether the current application's user interface displays using visual styles.
old-location: controls\IsAppThemed.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\userex\functions\isappthemed.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IsAppThemed, IsAppThemed function [Windows Controls], controls.IsAppThemed, controls.inet_IsAppThemed, inet_IsAppThemed, inet_IsAppThemed_cpp, uxtheme/IsAppThemed
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uxtheme.h
req.include-header: 
req.redist: 
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
 - Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
 - xamlpalwp.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
 - IsAppThemed
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll (version 1.0 or later)
req.irql: 
req.product: Windows UI
---

# IsAppThemed function


## -description


Reports whether the current application's user interface displays using visual styles.


## -parameters






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
The application has a visual style applied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The application does not have a visual style applied.

</td>
</tr>
</table>
 




## -remarks



Prior to Windows 8, a visual style can be turned off in Control Panel, so that an application can support visual styles but not have a visual style applied at a given time.

 In Windows 8, it is not possible to turn off visual styles.


Do not call this function during <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> or global objects contructors. This may cause invalid return values.



