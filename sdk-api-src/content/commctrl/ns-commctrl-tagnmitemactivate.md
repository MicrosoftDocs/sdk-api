---
UID: NS:commctrl.tagNMITEMACTIVATE
title: tagNMITEMACTIVATE
author: windows-sdk-content
description: Contains information about an LVN_ITEMACTIVATE notification code.
old-location: controls\NMITEMACTIVATE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmitemactivate.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "*LPNMITEMACTIVATE, LPNMITEMACTIVATE, LPNMITEMACTIVATE structure pointer [Windows Controls], LVKF_ALT, LVKF_CONTROL, LVKF_SHIFT, NMITEMACTIVATE, NMITEMACTIVATE structure [Windows Controls], _win32_NMITEMACTIVATE, _win32_NMITEMACTIVATE_cpp, commctrl/LPNMITEMACTIVATE, commctrl/NMITEMACTIVATE, controls.NMITEMACTIVATE, controls._win32_NMITEMACTIVATE, tagNMITEMACTIVATE"
ms.prod: windows
ms.technology: windows-sdk
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
 - NMITEMACTIVATE
product: Windows
targetos: Windows
req.typenames: NMITEMACTIVATE, *LPNMITEMACTIVATE
req.redist: 
---

# tagNMITEMACTIVATE structure


## -description


Contains information about an <a href="https://msdn.microsoft.com/en-us/library/Bb774843(v=VS.85).aspx">LVN_ITEMACTIVATE</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about this notification code. 


### -field iItem

Type: <b>int</b>

Index of the list-view item. If the item index is not used for the notification, this member will contain -1. 


### -field iSubItem

Type: <b>int</b>

One-based index of the subitem. If the subitem index is not used for the notification or the notification does not apply to a subitem, this member will contain zero. 


### -field uNewState

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

New item state. This member is zero for notification codes that do not use it. 


### -field uOldState

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Old item state. This member is zero for notification codes that do not use it. 


### -field uChanged

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Set of flags that indicate the item attributes that have changed. This member is zero for notifications that do not use it. Otherwise, it can have the same values as the 
					<b>mask</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Bb774760(v=VS.85).aspx">LVITEM</a> structure. 


### -field ptAction

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>


<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that indicates the location at which the event occurred, in client coordinates. This member is undefined for notification codes that do not use it. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPARAM</a></b>

Application-defined value of the item. This member is undefined for notification codes that do not use it. 


### -field uKeyFlags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Modifier keys that were pressed at the time of the activation. This member contains zero or a combination of the following flags: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVKF_ALT"></a><a id="lvkf_alt"></a><dl>
<dt><b>LVKF_ALT</b></dt>
</dl>
</td>
<td width="60%">
The  key is pressed. 

</td>
</tr>
<tr>
<td width="40%"><a id="LVKF_CONTROL"></a><a id="lvkf_control"></a><dl>
<dt><b>LVKF_CONTROL</b></dt>
</dl>
</td>
<td width="60%">
The  key is pressed. 

</td>
</tr>
<tr>
<td width="40%"><a id="LVKF_SHIFT"></a><a id="lvkf_shift"></a><dl>
<dt><b>LVKF_SHIFT</b></dt>
</dl>
</td>
<td width="60%">
The  key is pressed. 

</td>
</tr>
</table>
 

