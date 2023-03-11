---
UID: NS:commctrl.tagLHITTESTINFO
title: LHITTESTINFO (commctrl.h)
description: Used to get information about the link corresponding to a given location.
helpviewer_keywords: ["*PLHITTESTINFO","LHITTESTINFO","LHITTESTINFO structure [Windows Controls]","PLHITTESTINFO","PLHITTESTINFO structure pointer [Windows Controls]","commctrl/LHITTESTINFO","commctrl/PLHITTESTINFO","controls.LHITTESTINFO","controls.inet_LHITTESTINFO","inet_LHITTESTINFO","inet_LHITTESTINFO_cpp"]
old-location: controls\LHITTESTINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\syslink\structures\lhittestinfo.htm
ms.date: 12/05/2018
ms.keywords: '*PLHITTESTINFO, LHITTESTINFO, LHITTESTINFO structure [Windows Controls], PLHITTESTINFO, PLHITTESTINFO structure pointer [Windows Controls], commctrl/LHITTESTINFO, commctrl/PLHITTESTINFO, controls.LHITTESTINFO, controls.inet_LHITTESTINFO, inet_LHITTESTINFO, inet_LHITTESTINFO_cpp'
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
req.typenames: LHITTESTINFO, *PLHITTESTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLHITTESTINFO
 - commctrl/tagLHITTESTINFO
 - PLHITTESTINFO
 - commctrl/PLHITTESTINFO
 - LHITTESTINFO
 - commctrl/LHITTESTINFO
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
 - LHITTESTINFO
---

# LHITTESTINFO structure


## -description

Used to get information about the link corresponding to a given location.

## -struct-fields

### -field pt

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

Location for the hit-test, in client coordinates (not screen coordinates).

### -field item

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-litem">LITEM</a></b>

Receives information about the link corresponding to <b>pt</b>.

## -remarks

To convert from screen coordinates to client coordinates, use <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient">ScreenToClient</a>.

<div class="alert"><b>Note</b>  If the <a href="/windows/desktop/Controls/lm-hittest">LM_HITTEST</a> message succeeds, the system fills in <a href="/windows/desktop/api/commctrl/ns-commctrl-litem">LITEM.iLink</a> and <b>LITEM.szID</b>. If the <b>LM_HITTEST</b> message fails, do not assume that any information in <b>LITEM</b> is valid.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Controls/lm-hittest">LM_HITTEST</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-screentoclient">ScreenToClient</a>