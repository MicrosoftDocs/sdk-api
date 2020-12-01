---
UID: NS:commctrl.tagLITEM
title: LITEM (commctrl.h)
description: Used to set and retrieve information about a link item.
helpviewer_keywords: ["*PLITEM","LITEM","LITEM structure [Windows Controls]","PLITEM","PLITEM structure pointer [Windows Controls]","commctrl/LITEM","commctrl/PLITEM","controls.LITEM","controls.inet_LITEM","inet_LITEM","inet_LITEM_cpp"]
old-location: controls\LITEM.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\syslink\structures\litem.htm
ms.date: 12/05/2018
ms.keywords: '*PLITEM, LITEM, LITEM structure [Windows Controls], PLITEM, PLITEM structure pointer [Windows Controls], commctrl/LITEM, commctrl/PLITEM, controls.LITEM, controls.inet_LITEM, inet_LITEM, inet_LITEM_cpp'
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
targetos: Windows
req.typenames: LITEM, *PLITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLITEM
 - commctrl/tagLITEM
 - PLITEM
 - commctrl/PLITEM
 - LITEM
 - commctrl/LITEM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - LITEM
---

# LITEM structure


## -description

Used to set and retrieve information about a link item.

## -struct-fields

### -field mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Combination of one or more of the following flags, describing the information to set or retrieve:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LIF_ITEMINDEX</dt>
</dl>
</td>
<td width="60%">
Retrieve the numeric item index. Items are always accessed by index, therefore you must always set this flag and assign a value to <b>iLink</b>. To obtain the item ID you must set both LIF_ITEMINDEX and LIF_ITEMID.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LIF_STATE</dt>
</dl>
</td>
<td width="60%">
Use <b>stateMask</b>  to get or set the state of the link.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LIF_ITEMID</dt>
</dl>
</td>
<td width="60%">
Specify the item by the ID value given in <b>szID</b>.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LIF_URL</dt>
</dl>
</td>
<td width="60%">
Set or get the URL for this item.

</td>
</tr>
</table>

### -field iLink

Type: <b>int</b>

Value of type <b>int</b> that contains the item index. This numeric index is used to access a SysLink control link.

### -field state

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Combination of one or more of the following flags, describing the state of the item:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LIS_ENABLED</dt>
</dl>
</td>
<td width="60%">
The link can respond to user input. This is the default unless the entire control was created with <a href="/windows/desktop/winmsg/window-styles">WS_DISABLED</a>. In this case, all links are disabled.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LIS_FOCUSED</dt>
</dl>
</td>
<td width="60%">
The link has the keyboard focus. Pressing ENTER sends an NM_CLICK notification.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LIS_VISITED</dt>
</dl>
</td>
<td width="60%">
The link has been visited by the user. Changing the URL to one that has not been visited causes this flag to be cleared.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LIS_HOTTRACK</dt>
</dl>
</td>
<td width="60%">
 Indicates that the syslink control will highlight in a different color (COLOR_HIGHLIGHT) when the mouse hovers over the control.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LIS_DEFAULTCOLORS</dt>
</dl>
</td>
<td width="60%">
Enable custom text colors to be used.

</td>
</tr>
</table>

### -field stateMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Combination of flags describing which state item to get or set. Allowable items are identical to those allowed in <b>state</b>.

### -field szID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WCHAR</a>[MAX_LINKID_TEXT]</b>

<b>WCHAR</b> string that contains the ID name. The maximum number of characters in the array is MAX_LINKID_TEXT. The ID name cannot be used to access a SysLink control link. You use the item index to access the item.

### -field szUrl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WCHAR</a>[L_MAX_URL_LENGTH]</b>

<b>WCHAR</b> string that contains the URL represented by the link. The maximum number of characters in the array is L_MAX_URL_LENGTH.