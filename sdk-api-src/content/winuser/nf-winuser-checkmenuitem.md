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

# CheckMenuItem function


## -description


<p class="CCE_Message">[<b>CheckMenuItem</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/e1c669c7-7b56-428a-8433-d926330e42e1">SetMenuItemInfo</a>.
]

Sets the state of the specified menu item's check-mark attribute to either selected or clear. 


## -parameters




### -param hMenu

TBD


### -param uIDCheckItem [in]

Type: <b>UINT</b>

The menu item whose check-mark attribute is to be set, as determined by the <i>uCheck</i> parameter. 


### -param uCheck [in]

Type: <b>UINT</b>

The flags that control the interpretation of the <i>uIDCheckItem</i> parameter and the state of the menu item's check-mark attribute. This parameter can be a combination of either <b>MF_BYCOMMAND</b>, or <b>MF_BYPOSITION</b> and <b>MF_CHECKED</b> or <b>MF_UNCHECKED</b>. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_BYCOMMAND"></a><a id="mf_bycommand"></a><dl>
<dt><b>MF_BYCOMMAND</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Indicates that the <i>uIDCheckItem</i> parameter gives the identifier of the menu item. The <b>MF_BYCOMMAND</b> flag is the default, if neither the <b>MF_BYCOMMAND</b> nor <b>MF_BYPOSITION</b> flag is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_BYPOSITION"></a><a id="mf_byposition"></a><dl>
<dt><b>MF_BYPOSITION</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
Indicates that the <i>uIDCheckItem</i> parameter gives the zero-based relative position of the menu item.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_CHECKED"></a><a id="mf_checked"></a><dl>
<dt><b>MF_CHECKED</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
Sets the check-mark attribute to the selected state.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_UNCHECKED"></a><a id="mf_unchecked"></a><dl>
<dt><b>MF_UNCHECKED</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Sets the check-mark attribute to the clear state.

</td>
</tr>
</table>
 


#### - hmenu [in]

Type: <b>HMENU</b>

A handle to the menu of interest. 


## -returns



Type: <b>DWORD</b>

The return value specifies the previous state of the menu item (either <b>MF_CHECKED</b> or <b>MF_UNCHECKED</b>). If the menu item does not exist, the return value is –1. 




## -remarks



An item in a menu bar cannot have a check mark. 

The <i>uIDCheckItem</i> parameter identifies a item that opens a submenu or a command item. For a item that opens a submenu, the <i>uIDCheckItem</i> parameter must specify the position of the item. For a command item, the <i>uIDCheckItem</i> parameter can specify either the item's position or its identifier.


#### Examples

For an example, see <a href="using_menus.htm">Simulating Check Boxes in a Menu</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/893abf39-3475-48dc-920d-39a956463690">EnableMenuItem</a>



<a href="https://msdn.microsoft.com/69ecdcba-177c-4465-95ae-897ed4e96c2d">GetMenuItemID</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/7c0fb026-52ca-4ac6-bb94-1e72431b6056">SetMenuItemBitmaps</a>



<a href="https://msdn.microsoft.com/e1c669c7-7b56-428a-8433-d926330e42e1">SetMenuItemInfo</a>
 

 

