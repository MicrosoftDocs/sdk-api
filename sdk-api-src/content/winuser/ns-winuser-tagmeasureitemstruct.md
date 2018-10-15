---
UID: NS:winuser.tagMEASUREITEMSTRUCT
title: tagMEASUREITEMSTRUCT
author: windows-sdk-content
description: Informs the system of the dimensions of an owner-drawn control or menu item. This allows the system to process user interaction with the control correctly.
old-location: controls\MEASUREITEMSTRUCT.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxstructures\measureitemstruct.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*LPMEASUREITEMSTRUCT, *PMEASUREITEMSTRUCT, MEASUREITEMSTRUCT, MEASUREITEMSTRUCT structure [Windows Controls], ODT_COMBOBOX, ODT_LISTBOX, ODT_LISTVIEW, ODT_MENU, _win32_MEASUREITEMSTRUCT_str, _win32_MEASUREITEMSTRUCT_str_cpp, controls.MEASUREITEMSTRUCT, controls._win32_MEASUREITEMSTRUCT_str, tagMEASUREITEMSTRUCT, winuser/MEASUREITEMSTRUCT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - MEASUREITEMSTRUCT
product: Windows
targetos: Windows
req.typenames: MEASUREITEMSTRUCT, *PMEASUREITEMSTRUCT, *LPMEASUREITEMSTRUCT
req.redist: 
---

# tagMEASUREITEMSTRUCT structure


## -description


Informs the system of the dimensions of an owner-drawn control or menu item. This allows the system to process user interaction with the control correctly. 


## -struct-fields




### -field CtlType

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The control type. This member can be one of the values shown in the following table. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ODT_COMBOBOX"></a><a id="odt_combobox"></a><dl>
<dt><b>ODT_COMBOBOX</b></dt>
</dl>
</td>
<td width="60%">
Owner-drawn combo box

</td>
</tr>
<tr>
<td width="40%"><a id="ODT_LISTBOX"></a><a id="odt_listbox"></a><dl>
<dt><b>ODT_LISTBOX</b></dt>
</dl>
</td>
<td width="60%">
Owner-drawn list box

</td>
</tr>
<tr>
<td width="40%"><a id="ODT_LISTVIEW"></a><a id="odt_listview"></a><dl>
<dt><b>ODT_LISTVIEW</b></dt>
</dl>
</td>
<td width="60%">
Owner-draw list-view control

</td>
</tr>
<tr>
<td width="40%"><a id="ODT_MENU"></a><a id="odt_menu"></a><dl>
<dt><b>ODT_MENU</b></dt>
</dl>
</td>
<td width="60%">
Owner-drawn menu

</td>
</tr>
</table>
 


### -field CtlID

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The identifier of the combo box or list box. This member is not used for a menu. 


### -field itemID

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The identifier for a menu item or the position of a list box or combo box item. This value is specified for a list box only if it has the <a href="List_Box_Styles.htm">LBS_OWNERDRAWVARIABLE</a> style; this value is specified for a combo box only if it has the <a href="Combo_Box_Styles.htm">CBS_OWNERDRAWVARIABLE</a> style. 


### -field itemWidth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The width, in pixels, of a menu item. Before returning from the message, the owner of the owner-drawn menu item must fill this member. 


### -field itemHeight

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The height, in pixels, of an individual item in a list box or a menu. Before returning from the message, the owner of the owner-drawn combo box, list box, or menu item must fill out this member. 


### -field itemData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG_PTR</a></b>

The application-defined value associated with the menu item. For a control, this member specifies the value last assigned to the list box or combo box by the <a href="https://msdn.microsoft.com/df974fa2-114a-43ef-b0ac-0451c31d95cd">LB_SETITEMDATA</a> or <a href="https://msdn.microsoft.com/8be9eb57-a635-4c52-9838-556368813c74">CB_SETITEMDATA</a> message. If the list box or combo box has the LB_HASSTRINGS or CB_HASSTRINGS style, this value is initially zero. Otherwise, this value is initially the value passed to the list box or combo box in the 
					<i>lParam</i> parameter of one of the following messages: 
					

<ul>
<li>
<a href="https://msdn.microsoft.com/201bcb7b-e7d1-41e6-8eb7-a5864b659a52">CB_ADDSTRING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b9067b4e-afca-4c78-9ca2-c717b99c7459">CB_INSERTSTRING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/924d9232-6e38-49c3-aa3e-19efd46b01ba">LB_ADDSTRING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dfaa742d-2f42-4485-aed5-cda8ca9ba66c">LB_INSERTSTRING</a>
</li>
</ul>

## -remarks



The owner window of an owner-drawn control receives a pointer to the <b>MEASUREITEMSTRUCT</b> structure as the <i>lParam</i> parameter of a <a href="https://msdn.microsoft.com/6947bcd1-fd40-4238-b8f2-d4e06b90c0dc">WM_MEASUREITEM</a> message. The owner-drawn control sends this message to its owner window when the control is created. The owner then fills in the appropriate members in the structure for the control and returns. This structure is common to all owner-drawn controls except the owner-drawn button control whose size is predetermined by its window. 

If an application does not fill the appropriate members of <b>MEASUREITEMSTRUCT</b>, the control or menu item may not be drawn properly. 




## -see-also




<a href="https://msdn.microsoft.com/201bcb7b-e7d1-41e6-8eb7-a5864b659a52">CB_ADDSTRING</a>



<a href="https://msdn.microsoft.com/b9067b4e-afca-4c78-9ca2-c717b99c7459">CB_INSERTSTRING</a>



<a href="https://msdn.microsoft.com/8be9eb57-a635-4c52-9838-556368813c74">CB_SETITEMDATA</a>



<a href="https://msdn.microsoft.com/924d9232-6e38-49c3-aa3e-19efd46b01ba">LB_ADDSTRING</a>



<a href="https://msdn.microsoft.com/dfaa742d-2f42-4485-aed5-cda8ca9ba66c">LB_INSERTSTRING</a>



<a href="https://msdn.microsoft.com/df974fa2-114a-43ef-b0ac-0451c31d95cd">LB_SETITEMDATA</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/6947bcd1-fd40-4238-b8f2-d4e06b90c0dc">WM_MEASUREITEM</a>
 

 

