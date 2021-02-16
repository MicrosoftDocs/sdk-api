---
UID: NS:commctrl.tagNMREBARCHILDSIZE
title: NMREBARCHILDSIZE (commctrl.h)
description: Contains information used in handling the RBN_CHILDSIZE notification code.
helpviewer_keywords: ["*LPNMREBARCHILDSIZE","LPNMREBARCHILDSIZE","LPNMREBARCHILDSIZE structure pointer [Windows Controls]","NMREBARCHILDSIZE","NMREBARCHILDSIZE structure [Windows Controls]","_win32_NMREBARCHILDSIZE","_win32_NMREBARCHILDSIZE_cpp","commctrl/LPNMREBARCHILDSIZE","commctrl/NMREBARCHILDSIZE","controls.NMREBARCHILDSIZE","controls._win32_NMREBARCHILDSIZE"]
old-location: controls\NMREBARCHILDSIZE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\rebar\structures\nmrebarchildsize.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMREBARCHILDSIZE, LPNMREBARCHILDSIZE, LPNMREBARCHILDSIZE structure pointer [Windows Controls], NMREBARCHILDSIZE, NMREBARCHILDSIZE structure [Windows Controls], _win32_NMREBARCHILDSIZE, _win32_NMREBARCHILDSIZE_cpp, commctrl/LPNMREBARCHILDSIZE, commctrl/NMREBARCHILDSIZE, controls.NMREBARCHILDSIZE, controls._win32_NMREBARCHILDSIZE'
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
req.typenames: NMREBARCHILDSIZE, *LPNMREBARCHILDSIZE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMREBARCHILDSIZE
 - commctrl/tagNMREBARCHILDSIZE
 - LPNMREBARCHILDSIZE
 - commctrl/LPNMREBARCHILDSIZE
 - NMREBARCHILDSIZE
 - commctrl/NMREBARCHILDSIZE
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
 - NMREBARCHILDSIZE
---

# NMREBARCHILDSIZE structure


## -description

Contains information used in handling the <a href="/windows/desktop/Controls/rbn-childsize">RBN_CHILDSIZE</a> notification code.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about the notification.

### -field uBand

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based index of the band affected by the notification. This will be -1 if no band is affected.

### -field wID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Application-defined identifier of the band.

### -field rcChild

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>


<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the new size of the child window. This member can be changed during the notification to modify the child window's position and size.

### -field rcBand

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>


<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the new size of the band.