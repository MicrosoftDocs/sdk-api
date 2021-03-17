---
UID: NS:commctrl.tagNMOBJECTNOTIFY
title: NMOBJECTNOTIFY (commctrl.h)
description: Contains information used with the TBN_GETOBJECT, TCN_GETOBJECT, and PSN_GETOBJECT notification codes.
helpviewer_keywords: ["*LPNMOBJECTNOTIFY","LPNMOBJECTNOTIFY","LPNMOBJECTNOTIFY structure pointer [Windows Controls]","NMOBJECTNOTIFY","NMOBJECTNOTIFY structure [Windows Controls]","_win32_NMOBJECTNOTIFY","_win32_NMOBJECTNOTIFY_cpp","commctrl/LPNMOBJECTNOTIFY","commctrl/NMOBJECTNOTIFY","controls.NMOBJECTNOTIFY","controls._win32_NMOBJECTNOTIFY"]
old-location: controls\NMOBJECTNOTIFY.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmobjectnotify.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMOBJECTNOTIFY, LPNMOBJECTNOTIFY, LPNMOBJECTNOTIFY structure pointer [Windows Controls], NMOBJECTNOTIFY, NMOBJECTNOTIFY structure [Windows Controls], _win32_NMOBJECTNOTIFY, _win32_NMOBJECTNOTIFY_cpp, commctrl/LPNMOBJECTNOTIFY, commctrl/NMOBJECTNOTIFY, controls.NMOBJECTNOTIFY, controls._win32_NMOBJECTNOTIFY'
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
req.typenames: NMOBJECTNOTIFY, *LPNMOBJECTNOTIFY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMOBJECTNOTIFY
 - commctrl/tagNMOBJECTNOTIFY
 - LPNMOBJECTNOTIFY
 - commctrl/LPNMOBJECTNOTIFY
 - NMOBJECTNOTIFY
 - commctrl/NMOBJECTNOTIFY
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
 - NMOBJECTNOTIFY
---

# NMOBJECTNOTIFY structure


## -description

Contains information used with the <a href="/windows/desktop/Controls/tbn-getobject">TBN_GETOBJECT</a>, <a href="/windows/desktop/Controls/tcn-getobject">TCN_GETOBJECT</a>, and <a href="/windows/desktop/Controls/psn-getobject">PSN_GETOBJECT</a> notification codes.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about this notification.

### -field iItem

Type: <b>int</b>

A control-specific item identifier. This value will comply to item identification standards for the control sending the notification. However, this member is not used with the <a href="/windows/desktop/Controls/psn-getobject">PSN_GETOBJECT</a> notification code.

### -field piid

Type: <b>IID*</b>

A pointer to an interface identifier of the requested object.

### -field pObject

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an object provided by the window processing the notification code. The application processing the notification code sets this member.

### -field hResult

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

COM success or failure flags. The application processing the notification code sets this member.

### -field dwFlags