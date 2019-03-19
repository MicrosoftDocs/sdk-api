---
UID: NF:uxtheme.GetThemeSysBool
title: GetThemeSysBool function (uxtheme.h)
author: windows-sdk-content
description: Retrieves the Boolean value of a system metric.
old-location: controls\GetThemeSysBool.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemesysbool.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetThemeSysBool, GetThemeSysBool function [Windows Controls], TMT_FLATMENUS, controls.GetThemeSysBool, controls.inet_GetThemeSysBool, inet_GetThemeSysBool, inet_GetThemeSysBool_cpp, uxtheme/GetThemeSysBool
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
api_name:
 - GetThemeSysBool
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetThemeSysBool function


## -description


Retrieves the Boolean value of a system metric.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to theme data.


### -param iBoolId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the system Boolean metric desired. May be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TMT_FLATMENUS"></a><a id="tmt_flatmenus"></a><dl>
<dt><b>TMT_FLATMENUS</b></dt>
</dl>
</td>
<td width="60%">
Describes how menus are drawn. If <b>TRUE</b>, menus are drawn without shadows. If <b>FALSE</b>, menus have shadows underneath them.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Value of desired system metric.




## -remarks



If the theme data handle is not a <b>NULL</b> handle, this function returns the desired <b>BOOL</b> from the SysMetrics section of the visual style. If the theme data handle is <b>NULL</b>, this function returns the value of the specified system Boolean.



