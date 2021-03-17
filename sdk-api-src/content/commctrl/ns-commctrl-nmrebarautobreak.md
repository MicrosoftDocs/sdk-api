---
UID: NS:commctrl.tagNMREBARAUTOBREAK
title: NMREBARAUTOBREAK (commctrl.h)
description: Contains information used with the RBN_AUTOBREAK notification code.
helpviewer_keywords: ["*LPNMREBARAUTOBREAK","LPNMREBARAUTOBREAK","LPNMREBARAUTOBREAK structure pointer [Windows Controls]","NMREBARAUTOBREAK","NMREBARAUTOBREAK structure [Windows Controls]","commctrl/LPNMREBARAUTOBREAK","commctrl/NMREBARAUTOBREAK","controls.NMREBARAUTOBREAK","controls.inet_NMREBARAUTOBREAK","inet_NMREBARAUTOBREAK","inet_NMREBARAUTOBREAK_cpp"]
old-location: controls\NMREBARAUTOBREAK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\rebar\structures\nmrebarautobreak.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMREBARAUTOBREAK, LPNMREBARAUTOBREAK, LPNMREBARAUTOBREAK structure pointer [Windows Controls], NMREBARAUTOBREAK, NMREBARAUTOBREAK structure [Windows Controls], commctrl/LPNMREBARAUTOBREAK, commctrl/NMREBARAUTOBREAK, controls.NMREBARAUTOBREAK, controls.inet_NMREBARAUTOBREAK, inet_NMREBARAUTOBREAK, inet_NMREBARAUTOBREAK_cpp'
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
req.typenames: NMREBARAUTOBREAK, *LPNMREBARAUTOBREAK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMREBARAUTOBREAK
 - commctrl/tagNMREBARAUTOBREAK
 - LPNMREBARAUTOBREAK
 - commctrl/LPNMREBARAUTOBREAK
 - NMREBARAUTOBREAK
 - commctrl/NMREBARAUTOBREAK
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
 - NMREBARAUTOBREAK
---

# NMREBARAUTOBREAK structure


## -description

Contains information used with the <a href="/windows/desktop/Controls/rbn-autobreak">RBN_AUTOBREAK</a> notification code.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that provides additional information about this notification code.

### -field uBand

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based index of the band affected by the notification. This is -1 if no band is affected.

### -field wID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Application-defined ID of the band.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Application-defined value from the <b>lParam</b> member of the <a href="/windows/desktop/api/commctrl/ns-commctrl-rebarbandinfoa">REBARBANDINFO</a> structure that defines the rebar band.

### -field uMsg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

ID of the message.

### -field fStyleCurrent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Style of the specified band.

### -field fAutoBreak

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>BOOL</b> that indicates whether a break should occur.