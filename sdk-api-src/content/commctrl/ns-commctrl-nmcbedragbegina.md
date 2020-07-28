---
UID: NS:commctrl.__unnamed_struct_12
title: NMCBEDRAGBEGINA (commctrl.h)
description: Contains information used with the CBEN_DRAGBEGIN notification code.
helpviewer_keywords: ["*LPNMCBEDRAGBEGINA","*PNMCBEDRAGBEGINA","LPNMCBEDRAGBEGIN","LPNMCBEDRAGBEGIN structure pointer [Windows Controls]","NMCBEDRAGBEGIN","NMCBEDRAGBEGIN structure [Windows Controls]","NMCBEDRAGBEGINA","NMCBEDRAGBEGINW","_win32_NMCBEDRAGBEGIN","_win32_NMCBEDRAGBEGIN_cpp","commctrl/LPNMCBEDRAGBEGIN","commctrl/NMCBEDRAGBEGIN","commctrl/NMCBEDRAGBEGINA","commctrl/NMCBEDRAGBEGINW","controls.NMCBEDRAGBEGIN","controls._win32_NMCBEDRAGBEGIN"]
old-location: controls\NMCBEDRAGBEGIN.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboex\structures\nmcbedragbegin.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMCBEDRAGBEGINA, *PNMCBEDRAGBEGINA, LPNMCBEDRAGBEGIN, LPNMCBEDRAGBEGIN structure pointer [Windows Controls], NMCBEDRAGBEGIN, NMCBEDRAGBEGIN structure [Windows Controls], NMCBEDRAGBEGINA, NMCBEDRAGBEGINW, _win32_NMCBEDRAGBEGIN, _win32_NMCBEDRAGBEGIN_cpp, commctrl/LPNMCBEDRAGBEGIN, commctrl/NMCBEDRAGBEGIN, commctrl/NMCBEDRAGBEGINA, commctrl/NMCBEDRAGBEGINW, controls.NMCBEDRAGBEGIN, controls._win32_NMCBEDRAGBEGIN'
f1_keywords:
- commctrl/NMCBEDRAGBEGIN
dev_langs:
- c++
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMCBEDRAGBEGINW (Unicode) and NMCBEDRAGBEGINA (ANSI)
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
- NMCBEDRAGBEGIN
- NMCBEDRAGBEGINA
- NMCBEDRAGBEGINW
targetos: Windows
req.typenames: NMCBEDRAGBEGINA, *LPNMCBEDRAGBEGINA, *PNMCBEDRAGBEGINA
req.redist: 
ms.custom: 19H1
---

# NMCBEDRAGBEGINA structure


## -description


Contains information used with the <a href="https://docs.microsoft.com/windows/desktop/Controls/cben-dragbegin">CBEN_DRAGBEGIN</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about the notification code. 


### -field iItemid

Type: <b>int</b>

The zero-based index of the item being dragged. This value will always be -1, indicating that the item being dragged is the item displayed in the edit portion of the control. 


### -field szText

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">TCHAR</a></b>

The character buffer that contains the text of the item being dragged. 

## -remarks

> [!NOTE]
> The commctrl.h header defines NMCBEDRAGBEGIN as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

