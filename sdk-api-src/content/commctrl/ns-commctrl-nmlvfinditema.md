---
UID: NS:commctrl.tagNMLVFINDITEMA
title: NMLVFINDITEMA (commctrl.h)
description: Contains information the owner needs to find items requested by a virtual list-view control. This structure is used with the LVN_ODFINDITEM notification code. (ANSI)
helpviewer_keywords: ["*LPNMLVFINDITEMA","NMLVFINDITEM","NMLVFINDITEM structure [Windows Controls]","NMLVFINDITEMA","NMLVFINDITEMW","PNMLVFINDITEM","PNMLVFINDITEM structure pointer [Windows Controls]","_win32_NMLVFINDITEM","_win32_NMLVFINDITEM_cpp","commctrl/NMLVFINDITEM","commctrl/NMLVFINDITEMA","commctrl/NMLVFINDITEMW","commctrl/PNMLVFINDITEM","controls.NMLVFINDITEM","controls._win32_NMLVFINDITEM"]
old-location: controls\NMLVFINDITEM.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvfinditem.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMLVFINDITEMA, NMLVFINDITEM, NMLVFINDITEM structure [Windows Controls], NMLVFINDITEMA, NMLVFINDITEMW, PNMLVFINDITEM, PNMLVFINDITEM structure pointer [Windows Controls], _win32_NMLVFINDITEM, _win32_NMLVFINDITEM_cpp, commctrl/NMLVFINDITEM, commctrl/NMLVFINDITEMA, commctrl/NMLVFINDITEMW, commctrl/PNMLVFINDITEM, controls.NMLVFINDITEM, controls._win32_NMLVFINDITEM'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMLVFINDITEMW (Unicode) and NMLVFINDITEMA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NMLVFINDITEMA, *LPNMLVFINDITEMA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMLVFINDITEMA
 - commctrl/tagNMLVFINDITEMA
 - LPNMLVFINDITEMA
 - commctrl/LPNMLVFINDITEMA
 - NMLVFINDITEMA
 - commctrl/NMLVFINDITEMA
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
 - NMLVFINDITEM
 - NMLVFINDITEMA
 - NMLVFINDITEMW
---

# NMLVFINDITEMA structure


## -description

Contains information the owner needs to find items requested by a <a href="/windows/desktop/Controls/list-view-controls-overview">virtual list-view</a> control. This structure is used with the <a href="/windows/desktop/Controls/lvn-odfinditem">LVN_ODFINDITEM</a> notification code.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information on this notification code.

### -field iStart

Type: <b>int</b>

Index of the item at which the search will start.

### -field lvfi

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-lvfindinfoa">LVFINDINFO</a></b>


<a href="/windows/desktop/api/commctrl/ns-commctrl-lvfindinfoa">LVFINDINFO</a> structure that contains information necessary to perform a search.

## -remarks

> [!NOTE]
> The commctrl.h header defines NMLVFINDITEM as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
