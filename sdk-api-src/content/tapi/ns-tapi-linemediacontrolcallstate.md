---
UID: NS:tapi.linemediacontrolcallstate_tag
title: LINEMEDIACONTROLCALLSTATE (tapi.h)
description: The LINEMEDIACONTROLCALLSTATE structure describes a media action to be executed when detecting transitions into one or more call states. The lineSetMediaControl and TSPI_lineSetMediaControl functions use this structure.
helpviewer_keywords: ["*LPLINEMEDIACONTROLCALLSTATE","LINEMEDIACONTROLCALLSTATE","LINEMEDIACONTROLCALLSTATE structure [TAPI 2.2]","LPLINEMEDIACONTROLCALLSTATE","LPLINEMEDIACONTROLCALLSTATE structure pointer [TAPI 2.2]","_tapi2_linemediacontrolcallstate_str","tapi/LINEMEDIACONTROLCALLSTATE","tapi/LPLINEMEDIACONTROLCALLSTATE","tapi2.linemediacontrolcallstate_str"]
old-location: tapi2\linemediacontrolcallstate_str.htm
tech.root: tapi3
ms.assetid: c0768c2a-3015-41af-b32f-0b228a0f2ee6
ms.date: 12/05/2018
ms.keywords: '*LPLINEMEDIACONTROLCALLSTATE, LINEMEDIACONTROLCALLSTATE, LINEMEDIACONTROLCALLSTATE structure [TAPI 2.2], LPLINEMEDIACONTROLCALLSTATE, LPLINEMEDIACONTROLCALLSTATE structure pointer [TAPI 2.2], _tapi2_linemediacontrolcallstate_str, tapi/LINEMEDIACONTROLCALLSTATE, tapi/LPLINEMEDIACONTROLCALLSTATE, tapi2.linemediacontrolcallstate_str'
req.header: tapi.h
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
req.typenames: LINEMEDIACONTROLCALLSTATE, *LPLINEMEDIACONTROLCALLSTATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linemediacontrolcallstate_tag
 - tapi/linemediacontrolcallstate_tag
 - LPLINEMEDIACONTROLCALLSTATE
 - tapi/LPLINEMEDIACONTROLCALLSTATE
 - LINEMEDIACONTROLCALLSTATE
 - tapi/LINEMEDIACONTROLCALLSTATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEMEDIACONTROLCALLSTATE
---

# LINEMEDIACONTROLCALLSTATE structure


## -description

The 
<b>LINEMEDIACONTROLCALLSTATE</b> structure describes a media action to be executed when detecting transitions into one or more call states. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetmediacontrol">lineSetMediaControl</a> and 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetmediacontrol">TSPI_lineSetMediaControl</a> functions use this structure.

## -struct-fields

### -field dwCallStates

One or more call states. This member uses one of the 
<a href="/windows/desktop/Tapi/linecallstate--constants">LINECALLSTATE_ Constants</a>.

### -field dwMediaControl

Media control action. This member uses one of the 
<a href="/windows/desktop/Tapi/linemediacontrol--constants">LINEMEDIACONTROL_ Constants</a>.

## -remarks

This structure may not be extended.

The 
<b>LINEMEDIACONTROLCALLSTATE</b> structure defines a triple &lt;call state(s), media-control action&gt;. An array of these triples is passed to the 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetmediacontrol">lineSetMediaControl</a> function to set the media control actions triggered by the transition to the call state of the given call. When a transition to a listed call state is detected, the corresponding action on the media stream is invoked.

## -see-also

<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetmediacontrol">TSPI_lineSetMediaControl</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegeneratedigits">lineGenerateDigits</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetmediacontrol">lineSetMediaControl</a>