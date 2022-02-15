---
UID: NE:tapi3if.FINISH_MODE
title: FINISH_MODE (tapi3if.h)
description: The FINISH_MODE enum is used by applications to indicate the type of call finish required. Operations that the TAPI DLL performs vary depending on whether a call transfer is being completed or a call is being added to a conference.
helpviewer_keywords: ["FINISH_MODE","FINISH_MODE enumeration [TAPI 2.2]","FM_ASCONFERENCE","FM_ASTRANSFER","_tapi3_finish_mode","tapi3.finish_mode","tapi3if/FINISH_MODE","tapi3if/FM_ASCONFERENCE","tapi3if/FM_ASTRANSFER"]
old-location: tapi3\finish_mode.htm
tech.root: tapi3
ms.assetid: f0bf1d93-b6c3-473a-b7ee-2ebb984f42c5
ms.date: 12/05/2018
ms.keywords: FINISH_MODE, FINISH_MODE enumeration [TAPI 2.2], FM_ASCONFERENCE, FM_ASTRANSFER, _tapi3_finish_mode, tapi3.finish_mode, tapi3if/FINISH_MODE, tapi3if/FM_ASCONFERENCE, tapi3if/FM_ASTRANSFER
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: FINISH_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FINISH_MODE
 - tapi3if/FINISH_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - FINISH_MODE
---

# FINISH_MODE enumeration


## -description

The 
<b>FINISH_MODE</b> enum is used by applications to indicate the type of call finish required. Operations that the TAPI DLL performs vary depending on whether a call transfer is being completed or a call is being added to a conference.

## -enum-fields

### -field FM_ASTRANSFER:0

A call transfer is being finished.

### -field FM_ASCONFERENCE

A call is being added to a conference call.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish">ITBasicCallControl::Finish</a>
