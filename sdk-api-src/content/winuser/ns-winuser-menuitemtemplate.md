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

# MENUITEMTEMPLATE structure


## -description


Defines a menu item in a menu template. 


## -struct-fields




### -field mtOption

Type: <b>WORD</b>

One or more of the following predefined menu options that control the appearance of the menu item as shown in the following table. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_CHECKED"></a><a id="mf_checked"></a><dl>
<dt><b>MF_CHECKED</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item has a check mark next to it.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_GRAYED"></a><a id="mf_grayed"></a><dl>
<dt><b>MF_GRAYED</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item is initially inactive and drawn with a gray effect.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_HELP"></a><a id="mf_help"></a><dl>
<dt><b>MF_HELP</b></dt>
<dt>0x00004000L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item has a vertical separator to its left.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_MENUBARBREAK"></a><a id="mf_menubarbreak"></a><dl>
<dt><b>MF_MENUBARBREAK</b></dt>
<dt>0x00000020L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item is placed in a new column. The old and new columns are separated by a bar.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_MENUBREAK"></a><a id="mf_menubreak"></a><dl>
<dt><b>MF_MENUBREAK</b></dt>
<dt>0x00000040L</dt>
</dl>
</td>
<td width="60%">
Indicates that the menu item is placed in a new column.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_OWNERDRAW"></a><a id="mf_ownerdraw"></a><dl>
<dt><b>MF_OWNERDRAW</b></dt>
<dt>0x00000100L</dt>
</dl>
</td>
<td width="60%">
Indicates that the owner window of the menu is responsible for drawing all visual aspects of the menu item, including highlighted, selected, and inactive states. This option is not valid for an item in a menu bar.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_POPUP"></a><a id="mf_popup"></a><dl>
<dt><b>MF_POPUP</b></dt>
<dt>0x00000010L</dt>
</dl>
</td>
<td width="60%">
Indicates that the item is one that opens a drop-down menu or submenu.

</td>
</tr>
</table>
 


### -field mtID

Type: <b>WORD</b>

The menu item identifier of a command item; a command item sends a command message to its owner window. The <b>MENUITEMTEMPLATE</b> structure for an item that opens a drop-down menu or submenu does not contain the 
					<b>mtID</b> member. 


### -field mtString

Type: <b>WCHAR[1]</b>

The menu item. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/01736486-6dee-43fe-80a7-06c4cf13a23e">LoadMenuIndirect</a>



<a href="https://msdn.microsoft.com/7dd21370-9e26-4086-9ba1-98e79966c336">MENUITEMTEMPLATEHEADER</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>
 

 

