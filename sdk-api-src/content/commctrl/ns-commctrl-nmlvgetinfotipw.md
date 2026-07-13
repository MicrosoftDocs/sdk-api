---
UID: NS:commctrl.tagNMLVGETINFOTIPW
title: NMLVGETINFOTIPW (commctrl.h)
description: Contains and receives list-view item information needed to display a tooltip for an item. This structure is used with the LVN_GETINFOTIP notification code. (Unicode)
helpviewer_keywords: ["*LPNMLVGETINFOTIPW","LPNMLVGETINFOTIP","LPNMLVGETINFOTIP structure pointer [Windows Controls]","NMLVGETINFOTIP","NMLVGETINFOTIP structure [Windows Controls]","NMLVGETINFOTIPA","NMLVGETINFOTIPW","_win32_NMLVGETINFOTIP","_win32_NMLVGETINFOTIP_cpp","commctrl/LPNMLVGETINFOTIP","commctrl/NMLVGETINFOTIP","commctrl/NMLVGETINFOTIPA","commctrl/NMLVGETINFOTIPW","controls.NMLVGETINFOTIP","controls._win32_NMLVGETINFOTIP"]
old-location: controls\NMLVGETINFOTIP.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvgetinfotip.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMLVGETINFOTIPW, LPNMLVGETINFOTIP, LPNMLVGETINFOTIP structure pointer [Windows Controls], NMLVGETINFOTIP, NMLVGETINFOTIP structure [Windows Controls], NMLVGETINFOTIPA, NMLVGETINFOTIPW, _win32_NMLVGETINFOTIP, _win32_NMLVGETINFOTIP_cpp, commctrl/LPNMLVGETINFOTIP, commctrl/NMLVGETINFOTIP, commctrl/NMLVGETINFOTIPA, commctrl/NMLVGETINFOTIPW, controls.NMLVGETINFOTIP, controls._win32_NMLVGETINFOTIP'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMLVGETINFOTIPW (Unicode) and NMLVGETINFOTIPA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NMLVGETINFOTIPW, *LPNMLVGETINFOTIPW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMLVGETINFOTIPW
 - commctrl/tagNMLVGETINFOTIPW
 - LPNMLVGETINFOTIPW
 - commctrl/LPNMLVGETINFOTIPW
 - NMLVGETINFOTIPW
 - commctrl/NMLVGETINFOTIPW
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
 - NMLVGETINFOTIP
 - NMLVGETINFOTIPA
 - NMLVGETINFOTIPW
---

# NMLVGETINFOTIPW structure


## -description

Contains and receives list-view item information needed to display a tooltip for an item. This structure is used with the <a href="/windows/desktop/Controls/lvn-getinfotip">LVN_GETINFOTIP</a> notification code.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information on this notification code.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Either zero or LVGIT_UNFOLDED. See Remarks.

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Address of a string buffer that receives any additional text information. If 
					<b>dwFlags</b> is zero, this member will contain the existing item text. In this case, you should append any additional text onto the end of this string. The size of this buffer is specified by the 
					<b>cchTextMax</b> structure.

### -field cchTextMax

Type: <b>int</b>

Size, in characters, of the buffer pointed to by 
					<b>pszText</b>. Although you should never assume that this buffer will be of any particular size, the INFOTIPSIZE value can be used for design purposes.

### -field iItem

Type: <b>int</b>

Zero-based index of the item to which this structure refers.

### -field iSubItem

Type: <b>int</b>

One-based index of the subitem to which this structure refers. If this member is zero, the structure is referring to the item and not a subitem. This member is not currently used and will always be zero.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Application-defined value associated with the item. This member is not currently used and will always be zero.

## -remarks

An item is said to be folded when the currently displayed text is truncated. If LVGIT_UNFOLDED is returned in <b>dwFlags</b>, the full text of the item is already displayed, so there is no need to display it in the tooltip.




> [!NOTE]
> The commctrl.h header defines NMLVGETINFOTIP as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
