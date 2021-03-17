---
UID: NS:commctrl.tagNMCUSTOMTEXT
title: NMCUSTOMTEXT (commctrl.h)
description: Contains information used with custom text notification.
helpviewer_keywords: ["*LPNMCUSTOMTEXT","LPNMCUSTOMTEXT","LPNMCUSTOMTEXT structure pointer [Windows Controls]","NMCUSTOMTEXT","NMCUSTOMTEXT structure [Windows Controls]","_shell_NMCUSTOMTEXT","_shell_NMCUSTOMTEXT_cpp","commctrl/LPNMCUSTOMTEXT","commctrl/NMCUSTOMTEXT","controls.NMCUSTOMTEXT","controls._shell_NMCUSTOMTEXT"]
old-location: controls\NMCUSTOMTEXT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmcustomtext.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMCUSTOMTEXT, LPNMCUSTOMTEXT, LPNMCUSTOMTEXT structure pointer [Windows Controls], NMCUSTOMTEXT, NMCUSTOMTEXT structure [Windows Controls], _shell_NMCUSTOMTEXT, _shell_NMCUSTOMTEXT_cpp, commctrl/LPNMCUSTOMTEXT, commctrl/NMCUSTOMTEXT, controls.NMCUSTOMTEXT, controls._shell_NMCUSTOMTEXT'
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
req.typenames: NMCUSTOMTEXT, *LPNMCUSTOMTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMCUSTOMTEXT
 - commctrl/tagNMCUSTOMTEXT
 - LPNMCUSTOMTEXT
 - commctrl/LPNMCUSTOMTEXT
 - NMCUSTOMTEXT
 - commctrl/NMCUSTOMTEXT
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
 - NMCUSTOMTEXT
---

# NMCUSTOMTEXT structure


## -description

Contains information used with custom text notification.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about this notification.

### -field hDC

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

The device context to draw to.

### -field lpString

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

The string to draw.

### -field nCount

Type: <b>int</b>

Length of lpString.

### -field lpRect

Type: <b>LPRECT</b>

The rect to draw in.

### -field uFormat

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

One or more of the DT_* flags. For more information, see the description of the <i>uFormat</i> parameter of the <a href="/windows/desktop/api/winuser/nf-winuser-drawtext">DrawText</a> function. This may be <b>NULL</b>.

### -field fLink

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Whether the text is a link.