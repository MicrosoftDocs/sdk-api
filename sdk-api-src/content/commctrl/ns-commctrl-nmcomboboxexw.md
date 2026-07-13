---
UID: NS:commctrl.NMCOMBOBOXEXW
title: NMCOMBOBOXEXW (commctrl.h)
description: Contains information specific to ComboBoxEx items for use with notification codes. (Unicode)
helpviewer_keywords: ["*PNMCOMBOBOXEXW","NMCOMBOBOXEX","NMCOMBOBOXEX structure [Windows Controls]","NMCOMBOBOXEXA","NMCOMBOBOXEXW","PNMCOMBOBOXEX","PNMCOMBOBOXEX structure pointer [Windows Controls]","_win32_NMCOMBOBOXEX","_win32_NMCOMBOBOXEX_cpp","commctrl/NMCOMBOBOXEX","commctrl/NMCOMBOBOXEXA","commctrl/NMCOMBOBOXEXW","commctrl/PNMCOMBOBOXEX","controls.NMCOMBOBOXEX","controls._win32_NMCOMBOBOXEX"]
old-location: controls\NMCOMBOBOXEX.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboex\structures\nmcomboboxex.htm
ms.date: 12/05/2018
ms.keywords: '*PNMCOMBOBOXEXW, NMCOMBOBOXEX, NMCOMBOBOXEX structure [Windows Controls], NMCOMBOBOXEXA, NMCOMBOBOXEXW, PNMCOMBOBOXEX, PNMCOMBOBOXEX structure pointer [Windows Controls], _win32_NMCOMBOBOXEX, _win32_NMCOMBOBOXEX_cpp, commctrl/NMCOMBOBOXEX, commctrl/NMCOMBOBOXEXA, commctrl/NMCOMBOBOXEXW, commctrl/PNMCOMBOBOXEX, controls.NMCOMBOBOXEX, controls._win32_NMCOMBOBOXEX'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMCOMBOBOXEXW (Unicode) and NMCOMBOBOXEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NMCOMBOBOXEXW, *PNMCOMBOBOXEXW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PNMCOMBOBOXEXW
 - commctrl/PNMCOMBOBOXEXW
 - NMCOMBOBOXEXW
 - commctrl/NMCOMBOBOXEXW
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
 - NMCOMBOBOXEX
 - NMCOMBOBOXEXA
 - NMCOMBOBOXEXW
---

# NMCOMBOBOXEXW structure


## -description

Contains information specific to ComboBoxEx items for use with notification codes.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

The <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about the notification code.

### -field ceItem

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-comboboxexitema">COMBOBOXEXITEM</a></b>

The <a href="/windows/desktop/api/commctrl/ns-commctrl-comboboxexitema">COMBOBOXEXITEM</a> structure that holds item information specific to the current notification. Upon receiving a notification code, the <b>COMBOBOXEXITEM</b> structure holds information required for the owner to respond. The members of this structure are often used as fields for the owner to return values in response to the notification.

## -remarks

> [!NOTE]
> The commctrl.h header defines NMCOMBOBOXEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

