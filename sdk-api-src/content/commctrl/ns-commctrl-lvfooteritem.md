---
UID: NS:commctrl.tagLVFOOTERITEM
title: LVFOOTERITEM (commctrl.h)
description: Contains information on a footer item.
helpviewer_keywords: ["*LPLVFOOTERITEM","LPLVFOOTERITEM","LPLVFOOTERITEM structure pointer [Windows Controls]","LVFIF_STATE","LVFIF_TEXT","LVFIS_FOCUSED","LVFOOTERITEM","LVFOOTERITEM structure [Windows Controls]","_shell_LVFOOTERITEM","_shell_LVFOOTERITEM_cpp","commctrl/LPLVFOOTERITEM","commctrl/LVFOOTERITEM","controls.LVFOOTERITEM","controls._shell_LVFOOTERITEM"]
old-location: controls\LVFOOTERITEM.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvfooteritem.htm
ms.date: 12/05/2018
ms.keywords: '*LPLVFOOTERITEM, LPLVFOOTERITEM, LPLVFOOTERITEM structure pointer [Windows Controls], LVFIF_STATE, LVFIF_TEXT, LVFIS_FOCUSED, LVFOOTERITEM, LVFOOTERITEM structure [Windows Controls], _shell_LVFOOTERITEM, _shell_LVFOOTERITEM_cpp, commctrl/LPLVFOOTERITEM, commctrl/LVFOOTERITEM, controls.LVFOOTERITEM, controls._shell_LVFOOTERITEM'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: LVFOOTERITEM, *LPLVFOOTERITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLVFOOTERITEM
 - commctrl/tagLVFOOTERITEM
 - LPLVFOOTERITEM
 - commctrl/LPLVFOOTERITEM
 - LVFOOTERITEM
 - commctrl/LVFOOTERITEM
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
 - LVFOOTERITEM
---

# LVFOOTERITEM structure


## -description

Contains information on a footer item.

## -struct-fields

### -field mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Set of flags that specify which members of this structure contain data to be set or which members are being requested. This parameter must be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVFIF_TEXT"></a><a id="lvfif_text"></a><dl>
<dt><b>LVFIF_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The <b>pszText</b> member is valid input from the caller or is requested and thus should be set by the receiver.

</td>
</tr>
<tr>
<td width="40%"><a id="LVFIF_STATE"></a><a id="lvfif_state"></a><dl>
<dt><b>LVFIF_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>state</b> member is valid input from the caller or is requested and thus should be set by the receiver.

</td>
</tr>
</table>

### -field iItem

Type: <b>int</b>

The index of the item.

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

A pointer to a null-terminated, Unicode buffer. The calling process is responsible for allocating the buffer.

### -field cchTextMax

Type: <b>int</b>

The number of <b>WCHAR</b><b>s</b> in the buffer pointed to by <b>pszText</b>,  including the terminating <b>NULL</b>.

### -field state

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Indicates the item's state. The <b>stateMask</b> member indicates the valid bits of this member. Currently, <b>state</b> must be set to the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVFIS_FOCUSED"></a><a id="lvfis_focused"></a><dl>
<dt><b>LVFIS_FOCUSED</b></dt>
</dl>
</td>
<td width="60%">
Bit indicating focus state. Set if the item is in focus, otherwise cleared.

</td>
</tr>
</table>

### -field stateMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Value specifying which bits of the <b>state</b> member will be retrieved or modified. Currently, this value must be the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVFIS_FOCUSED"></a><a id="lvfis_focused"></a><dl>
<dt><b>LVFIS_FOCUSED</b></dt>
</dl>
</td>
<td width="60%">
The LVFIS_FOCUSED bit of member <b>state</b> is valid. For example, setting this member to LVFIS_FOCUSED will cause the focus state to be retrieved to member <b>state</b>.

</td>
</tr>
</table>

## -remarks

This structure is used with the <a href="/windows/desktop/api/commctrl/nf-commctrl-listview_getfooteritem">ListView_GetFooterItem</a> macro and the <a href="/windows/desktop/Controls/lvm-getfooteritem">LVM_GETFOOTERITEM</a> message.