---
UID: NS:commctrl.tagNMLVSCROLL
title: NMLVSCROLL (commctrl.h)
description: Provides information about a scrolling operation.
helpviewer_keywords: ["*LPNMLVSCROLL","LPNMLVSCROLL","LPNMLVSCROLL structure pointer [Windows Controls]","NMLVSCROLL","NMLVSCROLL structure [Windows Controls]","commctrl/LPNMLVSCROLL","commctrl/NMLVSCROLL","controls.NMLVSCROLL","controls.inet_NMLVSCROLL","inet_NMLVSCROLL","inet_NMLVSCROLL_cpp"]
old-location: controls\NMLVSCROLL.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvscroll.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMLVSCROLL, LPNMLVSCROLL, LPNMLVSCROLL structure pointer [Windows Controls], NMLVSCROLL, NMLVSCROLL structure [Windows Controls], commctrl/LPNMLVSCROLL, commctrl/NMLVSCROLL, controls.NMLVSCROLL, controls.inet_NMLVSCROLL, inet_NMLVSCROLL, inet_NMLVSCROLL_cpp'
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
req.typenames: NMLVSCROLL, *LPNMLVSCROLL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMLVSCROLL
 - commctrl/tagNMLVSCROLL
 - LPNMLVSCROLL
 - commctrl/LPNMLVSCROLL
 - NMLVSCROLL
 - commctrl/NMLVSCROLL
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
 - NMLVSCROLL
---

# NMLVSCROLL structure


## -description

Provides information about a scrolling operation.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about a <a href="/windows/desktop/Controls/lvn-endscroll">LVN_ENDSCROLL</a> or a <a href="/windows/desktop/Controls/lvn-beginscroll">LVN_BEGINSCROLL</a> notification code.

### -field dx

Type: <b>int</b>

Value of type <b>int</b> that specifies in pixels the horizontal position where a scrolling operation should begin or end.

### -field dy

Type: <b>int</b>

Value of type <b>int</b> that specifies in pixels the vertical position where a scrolling operation should begin or end.