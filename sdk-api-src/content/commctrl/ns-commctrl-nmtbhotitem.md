---
UID: NS:commctrl.tagNMTBHOTITEM
title: NMTBHOTITEM
author: windows-sdk-content
description: Contains information used with the TBN_HOTITEMCHANGE notification code.
old-location: controls\NMTBHOTITEM.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\nmtbhotitem.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPNMTBHOTITEM, HICF_ACCELERATOR, HICF_ARROWKEYS, HICF_DUPACCEL, HICF_ENTERING, HICF_LEAVING, HICF_LMOUSE, HICF_MOUSE, HICF_OTHER, HICF_RESELECT, HICF_TOGGLEDROPDOWN, LPNMTBHOTITEM, LPNMTBHOTITEM structure pointer [Windows Controls], NMTBHOTITEM, NMTBHOTITEM structure [Windows Controls], _win32_NMTBHOTITEM, _win32_NMTBHOTITEM_cpp, commctrl/LPNMTBHOTITEM, commctrl/NMTBHOTITEM, controls.NMTBHOTITEM, controls._win32_NMTBHOTITEM"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMTBHOTITEM
product: Windows
targetos: Windows
req.typenames: NMTBHOTITEM, *LPNMTBHOTITEM
req.redist: 
---

# NMTBHOTITEM structure


## -description


Contains information used with the <a href="https://msdn.microsoft.com/en-us/library/Bb787274(v=VS.85).aspx">TBN_HOTITEMCHANGE</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about the notification. 


### -field idOld

Type: <b>int</b>

Command identifier of the previously highlighted item. 


### -field idNew

Type: <b>int</b>

Command identifier of the item about to be highlighted. 


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Flags that indicate why the hot item has changed. This can be one or more of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HICF_ACCELERATOR"></a><a id="hicf_accelerator"></a><dl>
<dt><b>HICF_ACCELERATOR</b></dt>
</dl>
</td>
<td width="60%">
The change in the hot item was caused by a shortcut key. 

</td>
</tr>
<tr>
<td width="40%"><a id="HICF_ARROWKEYS"></a><a id="hicf_arrowkeys"></a><dl>
<dt><b>HICF_ARROWKEYS</b></dt>
</dl>
</td>
<td width="60%">
The change in the hot item was caused by an arrow key. 

</td>
</tr>
<tr>
<td width="40%"><a id="HICF_DUPACCEL"></a><a id="hicf_dupaccel"></a><dl>
<dt><b>HICF_DUPACCEL</b></dt>
</dl>
</td>
<td width="60%">
Modifies HICF_ACCELERATOR. If this flag is set, more than one item has the same shortcut key character. 

</td>
</tr>
<tr>
<td width="40%"><a id="HICF_ENTERING"></a><a id="hicf_entering"></a><dl>
<dt><b>HICF_ENTERING</b></dt>
</dl>
</td>
<td width="60%">
Modifies the other reason flags. If this flag is set, there is no previous hot item and 
						<b>idOld</b> does not contain valid information. 

</td>
</tr>
<tr>
<td width="40%"><a id="HICF_LEAVING"></a><a id="hicf_leaving"></a><dl>
<dt><b>HICF_LEAVING</b></dt>
</dl>
</td>
<td width="60%">
Modifies the other reason flags. If this flag is set, there is no new hot item and 
						<b>idNew</b> does not contain valid information. 

</td>
</tr>
<tr>
<td width="40%"><a id="HICF_LMOUSE"></a><a id="hicf_lmouse"></a><dl>
<dt><b>HICF_LMOUSE</b></dt>
</dl>
</td>
<td width="60%">
The change in the hot item resulted from a left-click mouse event. 

</td>
</tr>
<tr>
<td width="40%"><a id="HICF_MOUSE"></a><a id="hicf_mouse"></a><dl>
<dt><b>HICF_MOUSE</b></dt>
</dl>
</td>
<td width="60%">
The change in the hot item resulted from a mouse event. 

</td>
</tr>
<tr>
<td width="40%"><a id="HICF_OTHER"></a><a id="hicf_other"></a><dl>
<dt><b>HICF_OTHER</b></dt>
</dl>
</td>
<td width="60%">
The change in the hot item resulted from an event that could not be determined. This will most often be due to a change in focus or the <a href="https://msdn.microsoft.com/en-us/library/Bb787431(v=VS.85).aspx">TB_SETHOTITEM</a> message. 

</td>
</tr>
<tr>
<td width="40%"><a id="HICF_RESELECT"></a><a id="hicf_reselect"></a><dl>
<dt><b>HICF_RESELECT</b></dt>
</dl>
</td>
<td width="60%">
The change in the hot item resulted from the user entering the shortcut key for an item that was already hot. 

</td>
</tr>
<tr>
<td width="40%"><a id="HICF_TOGGLEDROPDOWN"></a><a id="hicf_toggledropdown"></a><dl>
<dt><b>HICF_TOGGLEDROPDOWN</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 5.80.</a> Causes the button to switch states. 

</td>
</tr>
</table>
 

