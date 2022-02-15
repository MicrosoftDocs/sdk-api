---
UID: NF:tapi3if.ITPhone.get_RingMode
title: ITPhone::get_RingMode (tapi3if.h)
description: The get_RingMode method retrieves the current ring mode for the phone.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_RingMode method","ITPhone.get_RingMode","ITPhone::get_RingMode","_tapi3_itphone_get_ringmode","get_RingMode","get_RingMode method [TAPI 2.2]","get_RingMode method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_ringmode","tapi3if/ITPhone::get_RingMode"]
old-location: tapi3\itphone_get_ringmode.htm
tech.root: tapi3
ms.assetid: 55f6a75c-dffb-46e7-8679-70c7d59ff5b4
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_RingMode method, ITPhone.get_RingMode, ITPhone::get_RingMode, _tapi3_itphone_get_ringmode, get_RingMode, get_RingMode method [TAPI 2.2], get_RingMode method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_ringmode, tapi3if/ITPhone::get_RingMode
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITPhone::get_RingMode
 - tapi3if/ITPhone::get_RingMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPhone.get_RingMode
---

# ITPhone::get_RingMode


## -description

The 
<b>get_RingMode</b> method retrieves the current ring mode for the phone.

The application must call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails.

## -parameters

### -param plRingMode [out]

Phone ring mode.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_ringmode">put_RingMode</a>