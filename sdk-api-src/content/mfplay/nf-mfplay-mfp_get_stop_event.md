---
UID: NF:mfplay.MFP_GET_STOP_EVENT
title: MFP_GET_STOP_EVENT macro (mfplay.h)
description: Casts an MFP_EVENT_HEADER pointer to an MFP_STOP_EVENT pointer.helpviewer_keywords: ["MFP_GET_STOP_EVENT","MFP_GET_STOP_EVENT macro [Media Foundation]","mf.mfp_get_stop_event","mfplay/MFP_GET_STOP_EVENT"]
old-location: mf\mfp_get_stop_event.htm
tech.root: medfound
ms.assetid: 3ca3fa23-1abf-49fc-96e3-f094b483c78f
ms.date: 12/05/2018
ms.keywords: MFP_GET_STOP_EVENT, MFP_GET_STOP_EVENT macro [Media Foundation], mf.mfp_get_stop_event, mfplay/MFP_GET_STOP_EVENT
f1_keywords:
- mfplay/MFP_GET_STOP_EVENT
dev_langs:
- c++
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- mfplay.h
api_name:
- MFP_GET_STOP_EVENT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFP_GET_STOP_EVENT macro


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Casts an <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/ns-mfplay-mfp_stop_event">MFP_STOP_EVENT</a> pointer.


## -parameters




### -param pHdr

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> structure.


## -remarks



The <b>eEventType</b> member of the input structure must be <b>MFP_EVENT_TYPE_STOP</b>. Otherwise, the macro returns <b>NULL</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-macros">Media Foundation Macros</a>
 

 

