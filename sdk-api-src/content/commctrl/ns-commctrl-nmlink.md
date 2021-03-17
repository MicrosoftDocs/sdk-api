---
UID: NS:commctrl.tagNMLINK
title: NMLINK (commctrl.h)
description: The NMLINK Contains notification information. Send this structure with the NM_CLICK or NM_RETURN messages.
helpviewer_keywords: ["*PNMLINK","NMLINK","NMLINK structure [Windows Controls]","PNMLINK","PNMLINK structure pointer [Windows Controls]","commctrl/NMLINK","commctrl/PNMLINK","controls.NMLINK","controls.inet_NMLINK_str","inet_NMLINK_str","inet_NMLINK_str_cpp"]
old-location: controls\NMLINK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\syslink\structures\nmlink.htm
ms.date: 12/05/2018
ms.keywords: '*PNMLINK, NMLINK, NMLINK structure [Windows Controls], PNMLINK, PNMLINK structure pointer [Windows Controls], commctrl/NMLINK, commctrl/PNMLINK, controls.NMLINK, controls.inet_NMLINK_str, inet_NMLINK_str, inet_NMLINK_str_cpp'
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
req.typenames: NMLINK, *PNMLINK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMLINK
 - commctrl/tagNMLINK
 - PNMLINK
 - commctrl/PNMLINK
 - NMLINK
 - commctrl/NMLINK
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
 - NMLINK
---

# NMLINK structure


## -description

The <b>NMLINK</b> Contains notification information. Send this structure with the <a href="/windows/desktop/Controls/nm-click-syslink">NM_CLICK</a> or <a href="/windows/desktop/Controls/nm-return">NM_RETURN</a> messages.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about the notification.

### -field item

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-litem">LITEM</a></b>


<a href="/windows/desktop/api/commctrl/ns-commctrl-litem">LITEM</a> structure that contains information about the link item.

## -see-also

<a href="/windows/desktop/api/commctrl/ns-commctrl-litem">LITEM</a>



<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a>



<a href="/windows/desktop/Controls/nm-click-syslink">NM_CLICK (syslink)</a>



<b>Reference</b>