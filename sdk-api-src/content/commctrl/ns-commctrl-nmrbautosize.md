---
UID: NS:commctrl.tagNMRBAUTOSIZE
title: NMRBAUTOSIZE (commctrl.h)
description: Contains information used in handling the RBN_AUTOSIZE notification codes.
helpviewer_keywords: ["*LPNMRBAUTOSIZE","LPNMRBAUTOSIZE","LPNMRBAUTOSIZE structure pointer [Windows Controls]","NMRBAUTOSIZE","NMRBAUTOSIZE structure [Windows Controls]","_win32_NMRBAUTOSIZE","_win32_NMRBAUTOSIZE_cpp","commctrl/LPNMRBAUTOSIZE","commctrl/NMRBAUTOSIZE","controls.NMRBAUTOSIZE","controls._win32_NMRBAUTOSIZE"]
old-location: controls\NMRBAUTOSIZE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\rebar\structures\nmrbautosize.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMRBAUTOSIZE, LPNMRBAUTOSIZE, LPNMRBAUTOSIZE structure pointer [Windows Controls], NMRBAUTOSIZE, NMRBAUTOSIZE structure [Windows Controls], _win32_NMRBAUTOSIZE, _win32_NMRBAUTOSIZE_cpp, commctrl/LPNMRBAUTOSIZE, commctrl/NMRBAUTOSIZE, controls.NMRBAUTOSIZE, controls._win32_NMRBAUTOSIZE'
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
req.typenames: NMRBAUTOSIZE, *LPNMRBAUTOSIZE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMRBAUTOSIZE
 - commctrl/tagNMRBAUTOSIZE
 - LPNMRBAUTOSIZE
 - commctrl/LPNMRBAUTOSIZE
 - NMRBAUTOSIZE
 - commctrl/NMRBAUTOSIZE
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
 - NMRBAUTOSIZE
---

# NMRBAUTOSIZE structure


## -description

Contains information used in handling the <a href="/windows/desktop/Controls/rbn-autosize">RBN_AUTOSIZE</a> notification codes.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about the notification.

### -field fChanged

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Member that indicates if the size or layout of the rebar control has changed (nonzero if a change occurred or zero otherwise).

### -field rcTarget

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>


<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the rectangle to which the rebar control tried to size itself.

### -field rcActual

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>


<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the rectangle to which the rebar control actually sized itself.