---
UID: NE:tapi3if.TAPI_GATHERTERM
title: TAPI_GATHERTERM (tapi3if.h)
description: The TAPI_GATHERTERM enum is used to describe the reasons why the TAPI Server terminated the gathering of digits on the call.
helpviewer_keywords: ["TAPI_GATHERTERM","TAPI_GATHERTERM enumeration [TAPI 2.2]","TGT_BUFFERFULL","TGT_CANCEL","TGT_FIRSTTIMEOUT","TGT_INTERTIMEOUT","TGT_TERMDIGIT","_tapi3_tapi_gatherterm","tapi3.tapi_gatherterm","tapi3if/TAPI_GATHERTERM","tapi3if/TGT_BUFFERFULL","tapi3if/TGT_CANCEL","tapi3if/TGT_FIRSTTIMEOUT","tapi3if/TGT_INTERTIMEOUT","tapi3if/TGT_TERMDIGIT"]
old-location: tapi3\tapi_gatherterm.htm
tech.root: tapi3
ms.assetid: 781266db-73a3-4202-922f-5c2d13bd3009
ms.date: 12/05/2018
ms.keywords: TAPI_GATHERTERM, TAPI_GATHERTERM enumeration [TAPI 2.2], TGT_BUFFERFULL, TGT_CANCEL, TGT_FIRSTTIMEOUT, TGT_INTERTIMEOUT, TGT_TERMDIGIT, _tapi3_tapi_gatherterm, tapi3.tapi_gatherterm, tapi3if/TAPI_GATHERTERM, tapi3if/TGT_BUFFERFULL, tapi3if/TGT_CANCEL, tapi3if/TGT_FIRSTTIMEOUT, tapi3if/TGT_INTERTIMEOUT, tapi3if/TGT_TERMDIGIT
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
req.typenames: TAPI_GATHERTERM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TAPI_GATHERTERM
 - tapi3if/TAPI_GATHERTERM
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
 - TAPI_GATHERTERM
---

# TAPI_GATHERTERM enumeration


## -description

The <b>TAPI_GATHERTERM</b> enum is used to describe the reasons why the TAPI Server terminated the gathering of digits on the call.

## -enum-fields

### -field TGT_BUFFERFULL:0x1

The requested number of digits has been gathered. The buffer is full.

### -field TGT_TERMDIGIT:0x2

One of the termination digits matched a received digit. The matched termination digit is the last digit in the buffer.

### -field TGT_FIRSTTIMEOUT:0x4

The first digit timeout expired. The buffer contains no digits.

### -field TGT_INTERTIMEOUT:0x8

The interdigit timeout expired. The buffer contains at least one digit.

### -field TGT_CANCEL:0x10

The request was canceled by this application, by another application, or because the call terminated.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itdigitsgatheredevent-get_gathertermination">ITDigitsGatheredEvent::get_GatherTermination</a>
