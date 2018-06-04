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

# _HD_HITTESTINFO structure


## -description


Contains information about a hit test. This structure is used with the <a href="https://msdn.microsoft.com/ff866bd1-9f2a-457c-921d-549610ab9088">HDM_HITTEST</a> message and it supersedes the <b>HD_HITTESTINFO</b> structure. 


## -struct-fields




### -field pt

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that contains the point to be hit test, in client coordinates. 


### -field flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The variable that receives information about the results of a hit test. This member can be one or more of the values listed below. Two of these values can be combined, such as when the position is above and to the left of the client area.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HHT_ABOVE"></a><a id="hht_above"></a><dl>
<dt><b>HHT_ABOVE</b></dt>
</dl>
</td>
<td width="60%">
The point is above the header control's bounding rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="HHT_BELOW"></a><a id="hht_below"></a><dl>
<dt><b>HHT_BELOW</b></dt>
</dl>
</td>
<td width="60%">
The point is below the header control's bounding rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="HHT_NOWHERE"></a><a id="hht_nowhere"></a><dl>
<dt><b>HHT_NOWHERE</b></dt>
</dl>
</td>
<td width="60%">
The point is inside the header control's bounding rectangle but is not over a header item.

</td>
</tr>
<tr>
<td width="40%"><a id="HHT_ONDIVIDER"></a><a id="hht_ondivider"></a><dl>
<dt><b>HHT_ONDIVIDER</b></dt>
</dl>
</td>
<td width="60%">
The point is on the divider between two header items.

</td>
</tr>
<tr>
<td width="40%"><a id="HHT_ONDIVOPEN"></a><a id="hht_ondivopen"></a><dl>
<dt><b>HHT_ONDIVOPEN</b></dt>
</dl>
</td>
<td width="60%">
The point is on the divider of an item that has a width of zero. Dragging the divider reveals the item instead of resizing the item to the left of the divider.

</td>
</tr>
<tr>
<td width="40%"><a id="HHT_ONHEADER"></a><a id="hht_onheader"></a><dl>
<dt><b>HHT_ONHEADER</b></dt>
</dl>
</td>
<td width="60%">
The point is inside the header control's bounding rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="HHT_ONFILTER"></a><a id="hht_onfilter"></a><dl>
<dt><b>HHT_ONFILTER</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 5.80</a> The point is over the filter area.

</td>
</tr>
<tr>
<td width="40%"><a id="HHT_ONFILTERBUTTON"></a><a id="hht_onfilterbutton"></a><dl>
<dt><b>HHT_ONFILTERBUTTON</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 5.80</a> The point is on the filter button.

</td>
</tr>
<tr>
<td width="40%"><a id="HHT_TOLEFT"></a><a id="hht_toleft"></a><dl>
<dt><b>HHT_TOLEFT</b></dt>
</dl>
</td>
<td width="60%">
The point is to the left of the header control's bounding rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="HHT_TORIGHT"></a><a id="hht_toright"></a><dl>
<dt><b>HHT_TORIGHT</b></dt>
</dl>
</td>
<td width="60%">
The point is to the right of the header control's bounding rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="HHT_ONITEMSTATEICON"></a><a id="hht_onitemstateicon"></a><dl>
<dt><b>HHT_ONITEMSTATEICON</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 6.00</a> and <b>Windows Vista. </b> The point is within the state icon of the item.  If style <a href="Header_Control_Styles.htm">HDS_CHECKBOXES</a> is specified, the point is within the checkbox of the item.

</td>
</tr>
<tr>
<td width="40%"><a id="HHT_ONDROPDOWN"></a><a id="hht_ondropdown"></a><dl>
<dt><b>HHT_ONDROPDOWN</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 6.00</a> and <b>Windows Vista.</b> The point is within the split button of the item.  The style HDF_SPLITBUTTON must be set on the item.

</td>
</tr>
<tr>
<td width="40%"><a id="HHT_ONOVERFLOW"></a><a id="hht_onoverflow"></a><dl>
<dt><b>HHT_ONOVERFLOW</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 6.00</a> and <b>Windows Vista.</b> The point is within the overflow button of the header control.  The style <a href="Header_Control_Styles.htm">HDS_OVERFLOW</a> must be set on the header control.

</td>
</tr>
</table>
 


### -field iItem

Type: <b>int</b>

If the hit test is successful, contains the index of the item at the hit test point.

