---
UID: NS:commctrl.tagNMHEADERW
title: NMHEADERW (commctrl.h)
author: windows-sdk-content
description: Contains information about header control notification messages. This structure supersedes the HD_NOTIFY structure.
old-location: controls\NMHEADER.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\structures\nmheader.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPNMHEADERW, 0, 1, 2, LPNMHEADER, LPNMHEADER structure pointer [Windows Controls], NMHEADER, NMHEADER structure [Windows Controls], NMHEADERA, NMHEADERW, _win32_NMHEADER, _win32_NMHEADER_cpp, commctrl/LPNMHEADER, commctrl/NMHEADER, commctrl/NMHEADERA, commctrl/NMHEADERW, controls.NMHEADER, controls._win32_NMHEADER"
ms.topic: struct
f1_keywords: ["commctrl/NMHEADER"]
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMHEADERW (Unicode) and NMHEADERA (ANSI)
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
 - NMHEADER
 - NMHEADERA
 - NMHEADERW
product: Windows
targetos: Windows
req.typenames: NMHEADERW, *LPNMHEADERW
req.redist: 
ms.custom: 19H1
---

# NMHEADERW structure


## -description


Contains information about header control notification messages. This structure supersedes the 
			<b>HD_NOTIFY</b> structure. 


## -struct-fields




### -field hdr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-_nmhdr">NMHDR</a></b>

A <a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-_nmhdr">NMHDR</a> structure that contains information about the notification message. 


### -field iItem

Type: <b>int</b>

The zero-based index of the header item that is the focus of the notification message. 


### -field iButton

Type: <b>int</b>

A value specifying the index of the mouse button used to generate the notification message. This member can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Left button

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Right button

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Middle button

</td>
</tr>
</table>
 


### -field pitem

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-_hd_itema">HDITEM</a>*</b>

An optional pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-_hd_itema">HDITEM</a> structure containing information about the item specified by 
					<b>iItem</b>. The 
					<b>mask</b> member of the <b>HDITEM</b> structure indicates which of its members are valid. 


## -remarks



While most header control notifications pass a pointer to an <b>NMHEADER</b> structure, only some of them use the <b>pitem</b> member to pass an <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-_hd_itema">HDITEM</a> structure. Those that do use <b>pitem</b> may not provide complete information about the item. To obtain more information about an item, use <a href="https://docs.microsoft.com/windows/desktop/Controls/hdm-getitem">HDM_GETITEM</a>.



