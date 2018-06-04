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

# HiliteMenuItem function


## -description


Adds or removes highlighting from an item in a menu bar. 


## -parameters




### -param hWnd

TBD


### -param hMenu

TBD


### -param uIDHiliteItem

TBD


### -param uHilite [in]

Type: <b>UINT</b>

Controls the interpretation of the <i>uItemHilite</i> parameter and indicates whether the menu item is highlighted. This parameter must be a combination of either <b>MF_BYCOMMAND</b> or <b>MF_BYPOSITION</b> and <b>MF_HILITE</b> or <b>MF_UNHILITE</b>. 

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
Indicates that <i>uItemHilite</i> gives the identifier of the menu item.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_BYPOSITION"></a><a id="mf_byposition"></a><dl>
<dt><b>MF_BYPOSITION</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
Indicates that <i>uItemHilite</i> gives the zero-based relative position of the menu item.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_HILITE"></a><a id="mf_hilite"></a><dl>
<dt><b>MF_HILITE</b></dt>
<dt>0x00000080L</dt>
</dl>
</td>
<td width="60%">
Highlights the menu item. If this flag is not specified, the highlighting is removed from the item.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_UNHILITE"></a><a id="mf_unhilite"></a><dl>
<dt><b>MF_UNHILITE</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Removes highlighting from the menu item.

</td>
</tr>
</table>
 


#### - hmenu [in]

Type: <b>HMENU</b>

A handle to the menu bar that contains the item. 


#### - hwnd [in]

Type: <b>HWND</b>

A handle to the window that contains the menu. 


#### - uItemHilite [in]

Type: <b>UINT</b>

The menu item. This parameter is either the identifier of the menu item or the offset of the menu item in the menu bar, depending on the value of the <i>uHilite</i> parameter. 


## -returns



Type: <b>BOOL</b>

If the menu item is set to the specified highlight state, the return value is nonzero.

If the menu item is not set to the specified highlight state, the return value is zero. 




## -remarks



The <b>MF_HILITE</b> and <b>MF_UNHILITE</b> flags can be used only with the <b>HiliteMenuItem</b> function; they cannot be used with the <a href="https://msdn.microsoft.com/2e6abd30-9ace-4a17-9cf6-8a45a71eecaf">ModifyMenu</a> function. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<a href="https://msdn.microsoft.com/2e6abd30-9ace-4a17-9cf6-8a45a71eecaf">ModifyMenu</a>



<b>Reference</b>
 

 

