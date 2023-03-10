---
UID: NE:tapi3if.CALLHUB_STATE
title: CALLHUB_STATE (tapi3if.h)
description: The CALLHUB_STATE enum is a state indicator returned by the ITCallHub::get_State method.
helpviewer_keywords: ["CALLHUB_STATE","CALLHUB_STATE enumeration [TAPI 2.2]","CHS_ACTIVE","CHS_IDLE","_tapi3_callhub_state","tapi3.callhub_state","tapi3if/CALLHUB_STATE","tapi3if/CHS_ACTIVE","tapi3if/CHS_IDLE"]
old-location: tapi3\callhub_state.htm
tech.root: tapi3
ms.assetid: 8ddfe1f5-2f4a-4b41-83ce-858a669afc31
ms.date: 12/05/2018
ms.keywords: CALLHUB_STATE, CALLHUB_STATE enumeration [TAPI 2.2], CHS_ACTIVE, CHS_IDLE, _tapi3_callhub_state, tapi3.callhub_state, tapi3if/CALLHUB_STATE, tapi3if/CHS_ACTIVE, tapi3if/CHS_IDLE
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
req.typenames: CALLHUB_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CALLHUB_STATE
 - tapi3if/CALLHUB_STATE
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
 - CALLHUB_STATE
---

# CALLHUB_STATE enumeration


## -description

The 
<b>CALLHUB_STATE</b> enum is a state indicator returned by the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallhub-get_state">ITCallHub::get_State</a> method.

## -enum-fields

### -field CHS_ACTIVE:0

The CallHub is active. There is at least one call that is not in the CS_DISCONNECTED state.

### -field CHS_IDLE

All calls associated with this CallHub are in the CS_DISCONNECTED state.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallhub-get_state">ITCallHub::get_State</a>
