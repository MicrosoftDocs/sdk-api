---
UID: NS:commctrl.tagNMHDFILTERBTNCLICK
title: NMHDFILTERBTNCLICK (commctrl.h)
description: Specifies or receives the attributes of a filter button click.
helpviewer_keywords: ["*LPNMHDFILTERBTNCLICK","LPNMHDFILTERBTNCLICK","LPNMHDFILTERBTNCLICK structure pointer [Windows Controls]","NMHDFILTERBTNCLICK","NMHDFILTERBTNCLICK structure [Windows Controls]","_win32_NMHDFILTERBTNCLICK_Structure","_win32_NMHDFILTERBTNCLICK_Structure_cpp","commctrl/LPNMHDFILTERBTNCLICK","commctrl/NMHDFILTERBTNCLICK","controls.NMHDFILTERBTNCLICK","controls._win32_NMHDFILTERBTNCLICK_Structure"]
old-location: controls\NMHDFILTERBTNCLICK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\structures\nmhdfilterbtnclick.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMHDFILTERBTNCLICK, LPNMHDFILTERBTNCLICK, LPNMHDFILTERBTNCLICK structure pointer [Windows Controls], NMHDFILTERBTNCLICK, NMHDFILTERBTNCLICK structure [Windows Controls], _win32_NMHDFILTERBTNCLICK_Structure, _win32_NMHDFILTERBTNCLICK_Structure_cpp, commctrl/LPNMHDFILTERBTNCLICK, commctrl/NMHDFILTERBTNCLICK, controls.NMHDFILTERBTNCLICK, controls._win32_NMHDFILTERBTNCLICK_Structure'
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
req.typenames: NMHDFILTERBTNCLICK, *LPNMHDFILTERBTNCLICK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMHDFILTERBTNCLICK
 - commctrl/tagNMHDFILTERBTNCLICK
 - LPNMHDFILTERBTNCLICK
 - commctrl/LPNMHDFILTERBTNCLICK
 - NMHDFILTERBTNCLICK
 - commctrl/NMHDFILTERBTNCLICK
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
 - NMHDFILTERBTNCLICK
---

# NMHDFILTERBTNCLICK structure


## -description

Specifies or receives the attributes of a filter button click.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

A handle of an <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information.

### -field iItem

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

The zero-based index of the control to which this structure refers.

### -field rc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the client rectangle for the filter button.

## -see-also

<a href="/windows/desktop/Controls/hdn-filterbtnclick">HDN_FILTERBTNCLICK</a>