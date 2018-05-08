---
UID: NS:commctrl.tagNMLVCUSTOMDRAW
title: tagNMLVCUSTOMDRAW
author: windows-driver-content
description: Contains information specific to an NM_CUSTOMDRAW (list view) notification code sent by a list-view control.
old-location: controls\NMLVCUSTOMDRAW.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvcustomdraw.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: "*LPNMLVCUSTOMDRAW, LPNMLVCUSTOMDRAW, LPNMLVCUSTOMDRAW structure pointer [Windows Controls], LVCDI_GROUP, LVCDI_ITEM, LVCDI_ITEMSLIST, LVGA_HEADER_CENTER, LVGA_HEADER_LEFT, LVGA_HEADER_RIGHT, NMLVCUSTOMDRAW, NMLVCUSTOMDRAW structure [Windows Controls], _win32_NMLVCUSTOMDRAW, _win32_NMLVCUSTOMDRAW_cpp, commctrl/LPNMLVCUSTOMDRAW, commctrl/NMLVCUSTOMDRAW, controls.NMLVCUSTOMDRAW, controls._win32_NMLVCUSTOMDRAW, tagNMLVCUSTOMDRAW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: commctrl.h
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
req.typenames: NMLVCUSTOMDRAW, *LPNMLVCUSTOMDRAW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	NMLVCUSTOMDRAW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagNMLVCUSTOMDRAW structure


## -description


Contains information specific to an <a href="https://msdn.microsoft.com/4e9b91e3-d042-4fd0-b063-a9e6ea9ad564">NM_CUSTOMDRAW (list view)</a> notification code sent by a list-view control. 


## -struct-fields




### -field nmcd

Type: <b><a href="https://msdn.microsoft.com/c8a990a9-fb39-46e7-a5d2-fc817ff46e1b">NMCUSTOMDRAW</a></b>


<a href="https://msdn.microsoft.com/c8a990a9-fb39-46e7-a5d2-fc817ff46e1b">NMCUSTOMDRAW</a> structure that contains general custom draw information. 


### -field clrText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

<b>COLORREF</b> value representing the color that will be used to display text foreground in the list-view control. 


### -field clrTextBk

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

<b>COLORREF</b> value representing the color that will be used to display text background in the list-view control. In <a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 6.0., </a> this member is ignored if the background image is set with the <a href="https://msdn.microsoft.com/8fdd363c-ac12-498b-80b7-aaa5741cfd76">LVM_SETBKIMAGE</a> message. 


### -field iSubItem

Type: <b>int</b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 4.71.</a> Index of the subitem that is being drawn. If the main item is being drawn, this member will be zero. 


### -field dwItemType

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 6.0. </a> 
					<b>DWORD</b> that contains the type of the item to draw. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVCDI_ITEM"></a><a id="lvcdi_item"></a><dl>
<dt><b>LVCDI_ITEM</b></dt>
</dl>
</td>
<td width="60%">
An item is to be drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCDI_GROUP"></a><a id="lvcdi_group"></a><dl>
<dt><b>LVCDI_GROUP</b></dt>
</dl>
</td>
<td width="60%">
A group is to be drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCDI_ITEMSLIST"></a><a id="lvcdi_itemslist"></a><dl>
<dt><b>LVCDI_ITEMSLIST</b></dt>
</dl>
</td>
<td width="60%">
Every item is to be drawn.

</td>
</tr>
</table>
 


### -field clrFace

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 6.0.</a> 
					<b>COLORREF</b> value representing the color that will be used to display the face of an item. 


### -field iIconEffect

Type: <b>int</b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 6.0.</a>  
					Value of type <b>int</b> that specifies the effect that is applied to an icon, such as Glow, Shadow, or Pulse. 


### -field iIconPhase

Type: <b>int</b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 6.0.</a>  
					Value of type <b>int</b> that specifies the phase of an icon. 


### -field iPartId

Type: <b>int</b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 6.0.</a>  
					Value of type <b>int</b> that specifies the ID of the part of an item to draw. 


### -field iStateId

Type: <b>int</b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 6.0.</a>  
					Value of type <b>int</b> that specifies the ID of the state of an item to draw. 


### -field rcText

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 6.0.</a>  
					<b>RECT</b> that specifies the rectangle in which the text is to be drawn. 


### -field uAlign

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 6.0.</a>  
					<b>UINT</b> that specifies how a group should be aligned. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVGA_HEADER_CENTER"></a><a id="lvga_header_center"></a><dl>
<dt><b>LVGA_HEADER_CENTER</b></dt>
</dl>
</td>
<td width="60%">
Center the group.

</td>
</tr>
<tr>
<td width="40%"><a id="LVGA_HEADER_LEFT"></a><a id="lvga_header_left"></a><dl>
<dt><b>LVGA_HEADER_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Align the group on the left.

</td>
</tr>
<tr>
<td width="40%"><a id="LVGA_HEADER_RIGHT"></a><a id="lvga_header_right"></a><dl>
<dt><b>LVGA_HEADER_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Align the group on the right.

</td>
</tr>
</table>
 


## -remarks



<div class="alert"><b>Note</b>  Comctl32.dll version 6 is not redistributable but it is included in Windows or later. To use Comctl32.dll version 6, specify it in a manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>.</div>
<div> </div>


