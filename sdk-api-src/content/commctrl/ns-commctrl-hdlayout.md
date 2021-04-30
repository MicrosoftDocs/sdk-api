---
UID: NS:commctrl._HD_LAYOUT
title: HDLAYOUT (commctrl.h)
description: Contains information used to set the size and position of a header control. HDLAYOUT is used with the HDM_LAYOUT message. This structure supersedes the HD_LAYOUT structure.
helpviewer_keywords: ["*LPHDLAYOUT","HDLAYOUT","HDLAYOUT structure [Windows Controls]","LPHDLAYOUT","LPHDLAYOUT structure pointer [Windows Controls]","_win32_HDLAYOUT","_win32_HDLAYOUT_cpp","commctrl/HDLAYOUT","commctrl/LPHDLAYOUT","controls.HDLAYOUT","controls._win32_HDLAYOUT"]
old-location: controls\HDLAYOUT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\structures\hdlayout.htm
ms.date: 12/05/2018
ms.keywords: '*LPHDLAYOUT, HDLAYOUT, HDLAYOUT structure [Windows Controls], LPHDLAYOUT, LPHDLAYOUT structure pointer [Windows Controls], _win32_HDLAYOUT, _win32_HDLAYOUT_cpp, commctrl/HDLAYOUT, commctrl/LPHDLAYOUT, controls.HDLAYOUT, controls._win32_HDLAYOUT'
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
req.typenames: HDLAYOUT, *LPHDLAYOUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HD_LAYOUT
 - commctrl/_HD_LAYOUT
 - LPHDLAYOUT
 - commctrl/LPHDLAYOUT
 - HDLAYOUT
 - commctrl/HDLAYOUT
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
 - HDLAYOUT
---

# HDLAYOUT structure


## -description

Contains information used to set the size and position of a header control. <b>HDLAYOUT</b> is used with the <a href="/windows/desktop/Controls/hdm-layout">HDM_LAYOUT</a> message. This structure supersedes the 
			<b>HD_LAYOUT</b> structure.

## -struct-fields

### -field prc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Structure that contains the coordinates of a rectangle that the header control will occupy.

### -field pwpos

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-windowpos">WINDOWPOS</a>*</b>

Structure that receives information about the appropriate size and position of the header control.