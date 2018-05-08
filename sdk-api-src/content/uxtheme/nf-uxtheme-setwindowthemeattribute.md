---
UID: NF:uxtheme.SetWindowThemeAttribute
title: SetWindowThemeAttribute function
author: windows-driver-content
description: Sets attributes to control how visual styles are applied to a specified window.
old-location: controls\SetWindowThemeAttribute.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\setwindowthemeattribute.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: SetWindowThemeAttribute, SetWindowThemeAttribute function [Windows Controls], WTA_NONCLIENT, controls.SetWindowThemeAttribute, controls.inet_SetWindowThemeAttribute, inet_SetWindowThemeAttribute, inet_SetWindowThemeAttribute_cpp, uxtheme/SetWindowThemeAttribute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BP_BUFFERFORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	UxTheme.dll
-	ext-ms-win-uxtheme-themes-l1-1-1.dll
-	xamlpalwp.dll
api_name:
-	SetWindowThemeAttribute
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# SetWindowThemeAttribute function


## -description


Sets attributes to control how visual styles are applied to a specified window.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a window to apply changes to.


### -param eAttribute [in]

Type: <b>enum WINDOWTHEMEATTRIBUTETYPE</b>

Value of type <a href="https://msdn.microsoft.com/1ad98d4a-7b88-426e-901a-8bfa8caa64d2">WINDOWTHEMEATTRIBUTETYPE</a> that specifies the type of attribute to set. The value of this parameter determines the type of data that should be passed in the <i>pvAttribute</i> parameter. Can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WTA_NONCLIENT"></a><a id="wta_nonclient"></a><dl>
<dt><b>WTA_NONCLIENT</b></dt>
</dl>
</td>
<td width="60%">
Specifies non-client related attributes. <i>pvAttribute</i> must be a pointer of type <a href="https://msdn.microsoft.com/00d147ef-32e3-40d8-9bdb-70eeaac3e8b6">WTA_OPTIONS</a>.

</td>
</tr>
</table>
 


### -param pvAttribute [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PVOID</a></b>

A pointer that specifies attributes to set. Type is determined by the value of the <i>eAttribute</i> value.


### -param cbAttribute [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the size, in bytes, of the data pointed to by <i>pvAttribute</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1ad98d4a-7b88-426e-901a-8bfa8caa64d2">WINDOWTHEMEATTRIBUTETYPE</a>
 

 

