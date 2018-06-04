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

# tagINITCOMMONCONTROLSEX structure


## -description


Carries information used to load common control classes from the dynamic-link library (DLL). This structure is used with the <a href="https://msdn.microsoft.com/a0ca2152-673e-4920-ae78-1421fdec1a05">InitCommonControlsEx</a> function. 


## -struct-fields




### -field dwSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The size of the structure, in bytes. 


### -field dwICC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The set of bit flags that indicate which common control classes will be loaded from the DLL. This can be a combination of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ICC_ANIMATE_CLASS"></a><a id="icc_animate_class"></a><dl>
<dt><b>ICC_ANIMATE_CLASS</b></dt>
</dl>
</td>
<td width="60%">
Load animate control class. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_BAR_CLASSES"></a><a id="icc_bar_classes"></a><dl>
<dt><b>ICC_BAR_CLASSES</b></dt>
</dl>
</td>
<td width="60%">
Load toolbar, status bar, trackbar, and tooltip control classes. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_COOL_CLASSES"></a><a id="icc_cool_classes"></a><dl>
<dt><b>ICC_COOL_CLASSES</b></dt>
</dl>
</td>
<td width="60%">
Load rebar control class. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_DATE_CLASSES"></a><a id="icc_date_classes"></a><dl>
<dt><b>ICC_DATE_CLASSES</b></dt>
</dl>
</td>
<td width="60%">
Load date and time picker control class. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_HOTKEY_CLASS"></a><a id="icc_hotkey_class"></a><dl>
<dt><b>ICC_HOTKEY_CLASS</b></dt>
</dl>
</td>
<td width="60%">
Load hot key control class. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_INTERNET_CLASSES"></a><a id="icc_internet_classes"></a><dl>
<dt><b>ICC_INTERNET_CLASSES</b></dt>
</dl>
</td>
<td width="60%">
Load IP address class. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_LINK_CLASS"></a><a id="icc_link_class"></a><dl>
<dt><b>ICC_LINK_CLASS</b></dt>
</dl>
</td>
<td width="60%">
Load a hyperlink control class. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_LISTVIEW_CLASSES"></a><a id="icc_listview_classes"></a><dl>
<dt><b>ICC_LISTVIEW_CLASSES</b></dt>
</dl>
</td>
<td width="60%">
Load list-view and header control classes. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_NATIVEFNTCTL_CLASS"></a><a id="icc_nativefntctl_class"></a><dl>
<dt><b>ICC_NATIVEFNTCTL_CLASS</b></dt>
</dl>
</td>
<td width="60%">
Load a native font control class. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_PAGESCROLLER_CLASS"></a><a id="icc_pagescroller_class"></a><dl>
<dt><b>ICC_PAGESCROLLER_CLASS</b></dt>
</dl>
</td>
<td width="60%">
Load pager control class. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_PROGRESS_CLASS"></a><a id="icc_progress_class"></a><dl>
<dt><b>ICC_PROGRESS_CLASS</b></dt>
</dl>
</td>
<td width="60%">
Load progress bar control class. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_STANDARD_CLASSES"></a><a id="icc_standard_classes"></a><dl>
<dt><b>ICC_STANDARD_CLASSES</b></dt>
</dl>
</td>
<td width="60%">
Load one of the intrinsic User32 control classes. The user controls include button, edit, static, listbox, combobox, and scroll bar. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_TAB_CLASSES"></a><a id="icc_tab_classes"></a><dl>
<dt><b>ICC_TAB_CLASSES</b></dt>
</dl>
</td>
<td width="60%">
Load tab and tooltip control classes. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_TREEVIEW_CLASSES"></a><a id="icc_treeview_classes"></a><dl>
<dt><b>ICC_TREEVIEW_CLASSES</b></dt>
</dl>
</td>
<td width="60%">
Load tree-view and tooltip control classes. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_UPDOWN_CLASS"></a><a id="icc_updown_class"></a><dl>
<dt><b>ICC_UPDOWN_CLASS</b></dt>
</dl>
</td>
<td width="60%">
Load up-down control class. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_USEREX_CLASSES"></a><a id="icc_userex_classes"></a><dl>
<dt><b>ICC_USEREX_CLASSES</b></dt>
</dl>
</td>
<td width="60%">
Load ComboBoxEx class. 

</td>
</tr>
<tr>
<td width="40%"><a id="ICC_WIN95_CLASSES"></a><a id="icc_win95_classes"></a><dl>
<dt><b>ICC_WIN95_CLASSES</b></dt>
</dl>
</td>
<td width="60%">
Load animate control, header, hot key, list-view, progress bar, status bar, tab, tooltip, toolbar, trackbar, tree-view, and up-down control classes. 

</td>
</tr>
</table>
 

