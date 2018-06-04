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

# tagDELETEITEMSTRUCT structure


## -description


Describes a deleted list box or combo box item. The <i>lParam</i> parameter of a <a href="https://msdn.microsoft.com/c3adf8fb-45f2-44f1-8821-6ffa7d76dc78">WM_DELETEITEM</a> message contains a pointer to this structure. When an item is removed from a list box or combo box or when a list box or combo box is destroyed, the system sends the <b>WM_DELETEITEM</b> message to the owner for each deleted item. 


The system sends a <a href="https://msdn.microsoft.com/c3adf8fb-45f2-44f1-8821-6ffa7d76dc78">WM_DELETEITEM</a> message only for items deleted from an owner-drawn list box (with the <a href="List_Box_Styles.htm">LBS_OWNERDRAWFIXED</a> or <a href="List_Box_Styles.htm">LBS_OWNERDRAWVARIABLE</a> style) or owner-drawn combo box (with the <a href="Combo_Box_Styles.htm">CBS_OWNERDRAWFIXED</a> or <a href="Combo_Box_Styles.htm">CBS_OWNERDRAWVARIABLE</a> style).


## -struct-fields




### -field CtlType

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies whether the item was deleted from a list box or a combo box. One of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ODT_LISTBOX"></a><a id="odt_listbox"></a><dl>
<dt><b>ODT_LISTBOX</b></dt>
</dl>
</td>
<td width="60%">
A list box.

</td>
</tr>
<tr>
<td width="40%"><a id="ODT_COMBOBOX"></a><a id="odt_combobox"></a><dl>
<dt><b>ODT_COMBOBOX</b></dt>
</dl>
</td>
<td width="60%">
A combo box.

</td>
</tr>
</table>
 


### -field CtlID

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The identifier of the list box or combo box. 


### -field itemID

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the item in the list box or combo box being removed. 


### -field hwndItem

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control. 


### -field itemData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG_PTR</a></b>

Application-defined data for the item. This value is passed to the control in the <i>lParam</i> parameter of the message that adds the item to the list box or combo box. 


## -see-also




<a href="https://msdn.microsoft.com/c3adf8fb-45f2-44f1-8821-6ffa7d76dc78">WM_DELETEITEM</a>
 

 

