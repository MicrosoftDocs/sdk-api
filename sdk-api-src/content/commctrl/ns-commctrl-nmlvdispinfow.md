---
UID: NS:commctrl.tagLVDISPINFOW
title: NMLVDISPINFOW (commctrl.h)
description: Contains information about an LVN_GETDISPINFO or LVN_SETDISPINFO notification code. This structure is the same as the LV_DISPINFO structure, but has been renamed to fit standard naming conventions. (Unicode)
helpviewer_keywords: ["*LPNMLVDISPINFOW","NMLVDISPINFO","NMLVDISPINFO structure [Windows Controls]","NMLVDISPINFOA","NMLVDISPINFOW","_win32_NMLVDISPINFO","_win32_NMLVDISPINFO_cpp","commctrl/NMLVDISPINFO","commctrl/NMLVDISPINFOA","commctrl/NMLVDISPINFOW","controls.NMLVDISPINFO","controls._win32_NMLVDISPINFO"]
old-location: controls\NMLVDISPINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvdispinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMLVDISPINFOW, NMLVDISPINFO, NMLVDISPINFO structure [Windows Controls], NMLVDISPINFOA, NMLVDISPINFOW, _win32_NMLVDISPINFO, _win32_NMLVDISPINFO_cpp, commctrl/NMLVDISPINFO, commctrl/NMLVDISPINFOA, commctrl/NMLVDISPINFOW, controls.NMLVDISPINFO, controls._win32_NMLVDISPINFO'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMLVDISPINFOW (Unicode) and NMLVDISPINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NMLVDISPINFOW, *LPNMLVDISPINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLVDISPINFOW
 - commctrl/tagLVDISPINFOW
 - LPNMLVDISPINFOW
 - commctrl/LPNMLVDISPINFOW
 - NMLVDISPINFOW
 - commctrl/NMLVDISPINFOW
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
 - NMLVDISPINFO
 - NMLVDISPINFOA
 - NMLVDISPINFOW
---

# NMLVDISPINFOW structure


## -description

Contains information about an <a href="/windows/desktop/Controls/lvn-getdispinfo">LVN_GETDISPINFO</a> or <a href="/windows/desktop/Controls/lvn-setdispinfo">LVN_SETDISPINFO</a> notification code. This structure is the same as the <b>LV_DISPINFO</b> structure, but has been renamed to fit standard naming conventions.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification code.

### -field item

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a></b>


<a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure that identifies the item or subitem. The structure either contains or receives information about the item. The <b>mask</b> member contains a set of bit flags that specify which item attributes are relevant.
For more information on the available bit flags, see <b>LVITEM</b>.

## -remarks

If the <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure is receiving item text, the <b>pszText</b> and <b>cchTextMax</b> members specify the address and size of a buffer. You can either copy text to the buffer or assign the address of a string to the <b>pszText</b> member. In the latter case, you must not change or delete the string until the corresponding item text is deleted or two additional <a href="/windows/desktop/Controls/lvn-getdispinfo">LVN_GETDISPINFO</a> messages have been sent. 


If you are handling the <a href="/windows/desktop/Controls/lvn-getdispinfo">LVN_GETDISPINFO</a> message, you can set the LVIF_DI_SETITEM flag in the <b>mask</b> member of the <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure. This tells the operating system to store the requested list item information and not ask for it again. For list-view controls with the <a href="/windows/desktop/Controls/list-view-window-styles">LVS_REPORT</a> style, this flag only applies to the first (subitem 0) column's information. The control will not store information for subitems.
		




> [!NOTE]
> The commctrl.h header defines NMLVDISPINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
