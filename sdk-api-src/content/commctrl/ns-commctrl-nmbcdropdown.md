---
UID: NS:commctrl.tagNMBCDROPDOWN
title: NMBCDROPDOWN (commctrl.h)
description: Contains information about a BCN_DROPDOWN notification.
helpviewer_keywords: ["*LPNMBCDROPDOWN","LPNMBCDROPDOWN","LPNMBCDROPDOWN structure pointer [Windows Controls]","NMBCDROPDOWN","NMBCDROPDOWN structure [Windows Controls]","_shell_NMBCDROPDOWN","_shell_NMBCDROPDOWN_cpp","commctrl/LPNMBCDROPDOWN","commctrl/NMBCDROPDOWN","controls.NMBCDROPDOWN","controls._shell_NMBCDROPDOWN"]
old-location: controls\NMBCDROPDOWN.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonstructures\nmbcdropdown.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMBCDROPDOWN, LPNMBCDROPDOWN, LPNMBCDROPDOWN structure pointer [Windows Controls], NMBCDROPDOWN, NMBCDROPDOWN structure [Windows Controls], _shell_NMBCDROPDOWN, _shell_NMBCDROPDOWN_cpp, commctrl/LPNMBCDROPDOWN, commctrl/NMBCDROPDOWN, controls.NMBCDROPDOWN, controls._shell_NMBCDROPDOWN'
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
req.typenames: NMBCDROPDOWN, *LPNMBCDROPDOWN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMBCDROPDOWN
 - commctrl/tagNMBCDROPDOWN
 - LPNMBCDROPDOWN
 - commctrl/LPNMBCDROPDOWN
 - NMBCDROPDOWN
 - commctrl/NMBCDROPDOWN
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
 - NMBCDROPDOWN
---

# NMBCDROPDOWN structure


## -description

Contains information about a <a href="/windows/desktop/Controls/bcn-dropdown">BCN_DROPDOWN</a> notification.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure containing information about the notification.

### -field rcButton

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the client area of the button.