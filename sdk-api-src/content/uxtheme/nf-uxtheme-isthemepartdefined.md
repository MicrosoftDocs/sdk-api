---
UID: NF:uxtheme.IsThemePartDefined
title: IsThemePartDefined function
author: windows-sdk-content
description: Retrieves whether a visual style has defined parameters for the specified part and state.
old-location: controls\IsThemePartDefined.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\isthemepartdefined.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IsThemePartDefined, IsThemePartDefined function [Windows Controls], controls.IsThemePartDefined, controls.inet_IsThemePartDefined, inet_IsThemePartDefined, inet_IsThemePartDefined_cpp, uxtheme/IsThemePartDefined
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
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
 - IsThemePartDefined
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- IsThemePartDefined
: 
---

# IsThemePartDefined function


## -description


Retrieves whether a visual style has defined parameters for the specified part and state.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a> to create an HTHEME.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Currently unused. The value should be 0. 


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
The theme has defined parameters for the specified <i>iPartId</i> and <i>iStateId</i>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The theme does not have defined parameters for the specified <i>iPartId</i> and <i>iStateId</i>

</td>
</tr>
</table>
 



