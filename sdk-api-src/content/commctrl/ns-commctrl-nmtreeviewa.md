---
UID: NS:commctrl.tagNMTREEVIEWA
title: NMTREEVIEWA (commctrl.h)
description: Contains information about a tree-view notification message. This structure is identical to the NM_TREEVIEW structure, but it has been renamed to follow current naming conventions. (ANSI)
helpviewer_keywords: ["*LPNMTREEVIEWA","LPNMTREEVIEW","LPNMTREEVIEW structure pointer [Windows Controls]","NMTREEVIEW","NMTREEVIEW structure [Windows Controls]","NMTREEVIEWA","NMTREEVIEWW","_win32_NMTREEVIEW","_win32_NMTREEVIEW_cpp","commctrl/LPNMTREEVIEW","commctrl/NMTREEVIEW","commctrl/NMTREEVIEWA","commctrl/NMTREEVIEWW","controls.NMTREEVIEW","controls._win32_NMTREEVIEW"]
old-location: controls\NMTREEVIEW.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtreeview.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMTREEVIEWA, LPNMTREEVIEW, LPNMTREEVIEW structure pointer [Windows Controls], NMTREEVIEW, NMTREEVIEW structure [Windows Controls], NMTREEVIEWA, NMTREEVIEWW, _win32_NMTREEVIEW, _win32_NMTREEVIEW_cpp, commctrl/LPNMTREEVIEW, commctrl/NMTREEVIEW, commctrl/NMTREEVIEWA, commctrl/NMTREEVIEWW, controls.NMTREEVIEW, controls._win32_NMTREEVIEW'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMTREEVIEWW (Unicode) and NMTREEVIEWA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NMTREEVIEWA, *LPNMTREEVIEWA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMTREEVIEWA
 - commctrl/tagNMTREEVIEWA
 - LPNMTREEVIEWA
 - commctrl/LPNMTREEVIEWA
 - NMTREEVIEWA
 - commctrl/NMTREEVIEWA
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
 - NMTREEVIEW
 - NMTREEVIEWA
 - NMTREEVIEWW
---

# NMTREEVIEWA structure


## -description

Contains information about a tree-view notification message. This structure is identical to the 
			<b>NM_TREEVIEW</b> structure, but it has been renamed to follow current naming conventions.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification message.

### -field action

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Notification-specific action flag. This member is used with the following notification codes.

<ul>
<li>
<a href="/windows/desktop/Controls/tvn-itemexpanding">TVN_ITEMEXPANDING</a>
</li>
<li>
<a href="/windows/desktop/Controls/tvn-itemexpanded">TVN_ITEMEXPANDED</a>
</li>
<li>
<a href="/windows/desktop/Controls/tvn-selchanging">TVN_SELCHANGING</a>
</li>
<li>
<a href="/windows/desktop/Controls/tvn-selchanged">TVN_SELCHANGED</a>
</li>
</ul>
For the possible action flag values, see <a href="/windows/desktop/Controls/tvm-expand">TVM_EXPAND</a> and <a href="/windows/desktop/Controls/tvn-selchanged">TVN_SELCHANGED</a>.

### -field itemOld

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-tvitema">TVITEM</a></b>


<a href="/windows/desktop/api/commctrl/ns-commctrl-tvitema">TVITEM</a> structure that contains information about the old item state. This member is zero for notification messages that do not use it.

### -field itemNew

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-tvitema">TVITEM</a></b>


<a href="/windows/desktop/api/commctrl/ns-commctrl-tvitema">TVITEM</a> structure that contains information about the new item state. This member is zero for notification messages that do not use it.

### -field ptDrag

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>


<a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that contains the client coordinates of the mouse at the time the event occurred that caused the notification message to be sent.

## -see-also

<a href="/windows/desktop/Controls/wm-notify">WM_NOTIFY</a>

## -remarks

> [!NOTE]
> The commctrl.h header defines NMTREEVIEW as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
