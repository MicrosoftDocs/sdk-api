---
UID: NS:commctrl.tagNMSELCHANGE
title: NMSELCHANGE (commctrl.h)
description: Carries information required to process the MCN_SELCHANGE notification code.
helpviewer_keywords: ["*LPNMSELCHANGE","*LPNMSELECT","LPNMSELCHANGE","LPNMSELCHANGE structure pointer [Windows Controls]","NMSELCHANGE","NMSELCHANGE structure [Windows Controls]","NMSELECT","_win32_NMSELCHANGE","_win32_NMSELCHANGE_cpp","commctrl/LPNMSELCHANGE","commctrl/NMSELCHANGE","controls.NMSELCHANGE","controls._win32_NMSELCHANGE"]
old-location: controls\NMSELCHANGE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\structures\nmselchange.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMSELCHANGE, *LPNMSELECT, LPNMSELCHANGE, LPNMSELCHANGE structure pointer [Windows Controls], NMSELCHANGE, NMSELCHANGE structure [Windows Controls], NMSELECT, _win32_NMSELCHANGE, _win32_NMSELCHANGE_cpp, commctrl/LPNMSELCHANGE, commctrl/NMSELCHANGE, controls.NMSELCHANGE, controls._win32_NMSELCHANGE'
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
req.typenames: NMSELCHANGE, *LPNMSELCHANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMSELCHANGE
 - commctrl/tagNMSELCHANGE
 - LPNMSELCHANGE
 - commctrl/LPNMSELCHANGE
 - NMSELCHANGE
 - commctrl/NMSELCHANGE
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
 - NMSELCHANGE
---

# NMSELCHANGE structure


## -description

Carries information required to process the <a href="/windows/desktop/Controls/mcn-selchange">MCN_SELCHANGE</a> notification code.

## -struct-fields

### -field nmhdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification.

### -field stSelStart

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>


<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the date for the first day in the user's selection range.

### -field stSelEnd

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>


<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the date for the last day in the user's selection range.