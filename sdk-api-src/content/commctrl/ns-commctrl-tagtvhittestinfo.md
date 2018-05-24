---
UID: NS:commctrl.tagTVHITTESTINFO
title: tagTVHITTESTINFO
author: windows-driver-content
description: Contains information used to determine the location of a point relative to a tree-view control.
old-location: controls\TVHITTESTINFO.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\tvhittestinfo.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: "*LPTVHITTESTINFO, LPTVHITTESTINFO, LPTVHITTESTINFO structure pointer [Windows Controls], TVHITTESTINFO, TVHITTESTINFO structure [Windows Controls], TVHT_ABOVE, TVHT_BELOW, TVHT_NOWHERE, TVHT_ONITEM, TVHT_ONITEMBUTTON, TVHT_ONITEMICON, TVHT_ONITEMINDENT, TVHT_ONITEMLABEL, TVHT_ONITEMRIGHT, TVHT_ONITEMSTATEICON, TVHT_TOLEFT, TVHT_TORIGHT, _win32_TVHITTESTINFO, _win32_TVHITTESTINFO_cpp, commctrl/LPTVHITTESTINFO, commctrl/TVHITTESTINFO, controls.TVHITTESTINFO, controls._win32_TVHITTESTINFO, tagTVHITTESTINFO"
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
req.typenames: TVHITTESTINFO, *LPTVHITTESTINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	TVHITTESTINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagTVHITTESTINFO structure


## -description


Contains information used to determine the location of a point relative to a tree-view control. This structure is used with the <a href="https://msdn.microsoft.com/18ea3737-f429-4c10-9133-3b5729aa36fa">TVM_HITTEST</a> message. The structure is identical to the 
			<b>TV_HITTESTINFO</b> structure, but it has been renamed to follow current naming conventions. 


## -struct-fields




### -field pt

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

Client coordinates of the point to test. 


### -field flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Variable that receives information about the results of a hit test. This member can be one or more of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TVHT_ABOVE"></a><a id="tvht_above"></a><dl>
<dt><b>TVHT_ABOVE</b></dt>
</dl>
</td>
<td width="60%">
Above the client area. 

</td>
</tr>
<tr>
<td width="40%"><a id="TVHT_BELOW"></a><a id="tvht_below"></a><dl>
<dt><b>TVHT_BELOW</b></dt>
</dl>
</td>
<td width="60%">
Below the client area. 

</td>
</tr>
<tr>
<td width="40%"><a id="TVHT_NOWHERE"></a><a id="tvht_nowhere"></a><dl>
<dt><b>TVHT_NOWHERE</b></dt>
</dl>
</td>
<td width="60%">
In the client area, but below the last item. 

</td>
</tr>
<tr>
<td width="40%"><a id="TVHT_ONITEM"></a><a id="tvht_onitem"></a><dl>
<dt><b>TVHT_ONITEM</b></dt>
</dl>
</td>
<td width="60%">
On the bitmap or label associated with an item. 

</td>
</tr>
<tr>
<td width="40%"><a id="TVHT_ONITEMBUTTON"></a><a id="tvht_onitembutton"></a><dl>
<dt><b>TVHT_ONITEMBUTTON</b></dt>
</dl>
</td>
<td width="60%">
On the button associated with an item. 

</td>
</tr>
<tr>
<td width="40%"><a id="TVHT_ONITEMICON"></a><a id="tvht_onitemicon"></a><dl>
<dt><b>TVHT_ONITEMICON</b></dt>
</dl>
</td>
<td width="60%">
On the bitmap associated with an item. 

</td>
</tr>
<tr>
<td width="40%"><a id="TVHT_ONITEMINDENT"></a><a id="tvht_onitemindent"></a><dl>
<dt><b>TVHT_ONITEMINDENT</b></dt>
</dl>
</td>
<td width="60%">
In the indentation associated with an item. 

</td>
</tr>
<tr>
<td width="40%"><a id="TVHT_ONITEMLABEL"></a><a id="tvht_onitemlabel"></a><dl>
<dt><b>TVHT_ONITEMLABEL</b></dt>
</dl>
</td>
<td width="60%">
On the label (string) associated with an item. 

</td>
</tr>
<tr>
<td width="40%"><a id="TVHT_ONITEMRIGHT"></a><a id="tvht_onitemright"></a><dl>
<dt><b>TVHT_ONITEMRIGHT</b></dt>
</dl>
</td>
<td width="60%">
In the area to the right of an item. 

</td>
</tr>
<tr>
<td width="40%"><a id="TVHT_ONITEMSTATEICON"></a><a id="tvht_onitemstateicon"></a><dl>
<dt><b>TVHT_ONITEMSTATEICON</b></dt>
</dl>
</td>
<td width="60%">
On the state icon for a tree-view item that is in a user-defined state. 

</td>
</tr>
<tr>
<td width="40%"><a id="TVHT_TOLEFT"></a><a id="tvht_toleft"></a><dl>
<dt><b>TVHT_TOLEFT</b></dt>
</dl>
</td>
<td width="60%">
To the left of the client area. 

</td>
</tr>
<tr>
<td width="40%"><a id="TVHT_TORIGHT"></a><a id="tvht_toright"></a><dl>
<dt><b>TVHT_TORIGHT</b></dt>
</dl>
</td>
<td width="60%">
To the right of the client area. 

</td>
</tr>
</table>
 


### -field hItem

Type: <b>HTREEITEM</b>

Handle to the item that occupies the point. 

