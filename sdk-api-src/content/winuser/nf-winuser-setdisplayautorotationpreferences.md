---
UID: NF:winuser.SetDisplayAutoRotationPreferences
title: SetDisplayAutoRotationPreferences function
author: windows-sdk-content
description: Sets the orientation preferences of the display.
old-location: gdi\setdisplayautorotationpreferences.htm
tech.root: gdi
ms.assetid: 95679AAC-9C04-4E21-BD34-A86F069B8AE3
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ORIENTATION_PREFERENCE_LANDSCAPE, ORIENTATION_PREFERENCE_LANDSCAPE_FLIPPED, ORIENTATION_PREFERENCE_NONE, ORIENTATION_PREFERENCE_PORTRAIT, ORIENTATION_PREFERENCE_PORTRAIT_FLIPPED, SetDisplayAutoRotationPreferences, SetDisplayAutoRotationPreferences function [Windows GDI], gdi.setdisplayautorotationpreferences, winuser/SetDisplayAutoRotationPreferences
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-NTUser-rotationmanager-l1-1-1.dll
 - ext-ms-win-ntuser-rotationmanager-l1-1-0.dll
api_name:
 - SetDisplayAutoRotationPreferences
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetDisplayAutoRotationPreferences function


## -description


Sets the orientation preferences of the display.


## -parameters




### -param orientation [in]

Type: <b>ORIENTATION_PREFERENCE</b>

A combination of <b>ORIENTATION_PREFERENCE</b>-typed values that are combined by using a bitwise OR operation. The resulting value specifies the orientation preferences of the display. Here are possible values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ORIENTATION_PREFERENCE_NONE"></a><a id="orientation_preference_none"></a><dl>
<dt><b>ORIENTATION_PREFERENCE_NONE</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
No display orientation is specified.


</td>
</tr>
<tr>
<td width="40%"><a id="ORIENTATION_PREFERENCE_LANDSCAPE"></a><a id="orientation_preference_landscape"></a><dl>
<dt><b>ORIENTATION_PREFERENCE_LANDSCAPE</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Specifies that the display can be oriented in landscape mode where the width of the display viewing area is greater than the height.


</td>
</tr>
<tr>
<td width="40%"><a id="ORIENTATION_PREFERENCE_PORTRAIT"></a><a id="orientation_preference_portrait"></a><dl>
<dt><b>ORIENTATION_PREFERENCE_PORTRAIT</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Specifies that the display can be oriented in portrait mode where the height of the display viewing area is greater than the width.


</td>
</tr>
<tr>
<td width="40%"><a id="ORIENTATION_PREFERENCE_LANDSCAPE_FLIPPED"></a><a id="orientation_preference_landscape_flipped"></a><dl>
<dt><b>ORIENTATION_PREFERENCE_LANDSCAPE_FLIPPED</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
Specifies that the display can be oriented in flipped landscape mode where the width of the display viewing area is greater than the height. This landscape mode is flipped 180 degrees from <b>ORIENTATION_PREFERENCE_LANDSCAPE</b> mode.


</td>
</tr>
<tr>
<td width="40%"><a id="ORIENTATION_PREFERENCE_PORTRAIT_FLIPPED"></a><a id="orientation_preference_portrait_flipped"></a><dl>
<dt><b>ORIENTATION_PREFERENCE_PORTRAIT_FLIPPED</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Specifies that the display can be oriented in flipped portrait mode where the height of the display viewing area is greater than the width. This portrait mode is flipped 180 degrees from the <b>ORIENTATION_PREFERENCE_PORTRAIT</b> mode.


</td>
</tr>
</table>
 


## -returns



Type: <b>BOOL</b>

If this function set the orientation preferences, the return value is nonzero.

If the orientation preferences weren't set, the return value is zero.




## -remarks



An app can remove  the orientation preferences of the display after it sets them by passing  <b>ORIENTATION_PREFERENCE_NONE</b> to <b>SetDisplayAutoRotationPreferences</b>. An app can change the orientation preferences of the display by passing  a different combination of <b>ORIENTATION_PREFERENCE</b>-typed values to <b>SetDisplayAutoRotationPreferences</b>. 




## -see-also




<a href="https://msdn.microsoft.com/2E412DAA-1855-4CB1-856C-4486A895E63D">GetDisplayAutoRotationPreferences</a>
 

 

