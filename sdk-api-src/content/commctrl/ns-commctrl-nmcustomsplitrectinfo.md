---
UID: NS:commctrl.tagNMCUSTOMSPLITRECTINFO
title: NMCUSTOMSPLITRECTINFO (commctrl.h)
description: Contains information about the two rectangles of a split button. Sent with the NM_GETCUSTOMSPLITRECT notification.
helpviewer_keywords: ["*LPNMCUSTOMSPLITRECTINFO","LPNMCUSTOMSPLITRECTINFO","LPNMCUSTOMSPLITRECTINFO structure pointer [Windows Controls]","NMCUSTOMSPLITRECTINFO","NMCUSTOMSPLITRECTINFO structure [Windows Controls]","_shell_NMCUSTOMSPLITRECTINFO","_shell_NMCUSTOMSPLITRECTINFO_cpp","commctrl/LPNMCUSTOMSPLITRECTINFO","commctrl/NMCUSTOMSPLITRECTINFO","controls.NMCUSTOMSPLITRECTINFO","controls._shell_NMCUSTOMSPLITRECTINFO"]
old-location: controls\NMCUSTOMSPLITRECTINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmcustomsplitrectinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMCUSTOMSPLITRECTINFO, LPNMCUSTOMSPLITRECTINFO, LPNMCUSTOMSPLITRECTINFO structure pointer [Windows Controls], NMCUSTOMSPLITRECTINFO, NMCUSTOMSPLITRECTINFO structure [Windows Controls], _shell_NMCUSTOMSPLITRECTINFO, _shell_NMCUSTOMSPLITRECTINFO_cpp, commctrl/LPNMCUSTOMSPLITRECTINFO, commctrl/NMCUSTOMSPLITRECTINFO, controls.NMCUSTOMSPLITRECTINFO, controls._shell_NMCUSTOMSPLITRECTINFO'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: NMCUSTOMSPLITRECTINFO, *LPNMCUSTOMSPLITRECTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMCUSTOMSPLITRECTINFO
 - commctrl/tagNMCUSTOMSPLITRECTINFO
 - LPNMCUSTOMSPLITRECTINFO
 - commctrl/LPNMCUSTOMSPLITRECTINFO
 - NMCUSTOMSPLITRECTINFO
 - commctrl/NMCUSTOMSPLITRECTINFO
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
 - NMCUSTOMSPLITRECTINFO
---

# NMCUSTOMSPLITRECTINFO structure


## -description

Contains information about the two rectangles of a split button. Sent with the <a href="/windows/desktop/Controls/nm-getcustomsplitrect">NM_GETCUSTOMSPLITRECT</a> notification.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about the notification.

### -field rcClient

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that describes the client area the button occupies.

### -field rcButton

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that describes the rectangle that does not contain the drop-down arrow.

### -field rcSplit

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that describes the rectangle that contains the drop-down arrow.

## -remarks

This information is used to draw the button. The button must be of style <a href="/windows/desktop/Controls/button-styles">BS_SPLITBUTTON</a> or <a href="/windows/desktop/Controls/button-styles">BS_DEFSPLITBUTTON</a>