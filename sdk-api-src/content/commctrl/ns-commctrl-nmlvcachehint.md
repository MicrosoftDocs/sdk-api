---
UID: NS:commctrl.tagNMLVCACHEHINT
title: NMLVCACHEHINT (commctrl.h)
description: Contains information used to update the cached item information for use with a virtual list view.
helpviewer_keywords: ["*LPNMLVCACHEHINT","NMLVCACHEHINT","NMLVCACHEHINT structure [Windows Controls]","PNMLVCACHEHINT","PNMLVCACHEHINT structure pointer [Windows Controls]","_win32_NMLVCACHEHINT","_win32_NMLVCACHEHINT_cpp","commctrl/NMLVCACHEHINT","commctrl/PNMLVCACHEHINT","controls.NMLVCACHEHINT","controls._win32_NMLVCACHEHINT"]
old-location: controls\NMLVCACHEHINT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvcachehint.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMLVCACHEHINT, NMLVCACHEHINT, NMLVCACHEHINT structure [Windows Controls], PNMLVCACHEHINT, PNMLVCACHEHINT structure pointer [Windows Controls], _win32_NMLVCACHEHINT, _win32_NMLVCACHEHINT_cpp, commctrl/NMLVCACHEHINT, commctrl/PNMLVCACHEHINT, controls.NMLVCACHEHINT, controls._win32_NMLVCACHEHINT'
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
req.typenames: NMLVCACHEHINT, *LPNMLVCACHEHINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMLVCACHEHINT
 - commctrl/tagNMLVCACHEHINT
 - LPNMLVCACHEHINT
 - commctrl/LPNMLVCACHEHINT
 - NMLVCACHEHINT
 - commctrl/NMLVCACHEHINT
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
 - NMLVCACHEHINT
---

# NMLVCACHEHINT structure


## -description

Contains information used to update the cached item information for use with a <a href="/windows/desktop/Controls/list-view-controls-overview">virtual list view</a>.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification message.

### -field iFrom

Type: <b>int</b>

Starting index of the requested range of items. This value is inclusive.

### -field iTo

Type: <b>int</b>

Ending index of the requested range of items. This value is inclusive.