---
UID: NF:tapi3if.ITPhone.put_RingMode
title: ITPhone::put_RingMode (tapi3if.h)
description: The put_RingMode method requests that the phone change its ring mode.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","put_RingMode method","ITPhone.put_RingMode","ITPhone::put_RingMode","_tapi3_itphone_put_ringmode","put_RingMode","put_RingMode method [TAPI 2.2]","put_RingMode method [TAPI 2.2]","ITPhone interface","tapi3.itphone_put_ringmode","tapi3if/ITPhone::put_RingMode"]
old-location: tapi3\itphone_put_ringmode.htm
tech.root: tapi3
ms.assetid: f693bf24-540d-4509-bf0c-01be27f823f8
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],put_RingMode method, ITPhone.put_RingMode, ITPhone::put_RingMode, _tapi3_itphone_put_ringmode, put_RingMode, put_RingMode method [TAPI 2.2], put_RingMode method [TAPI 2.2],ITPhone interface, tapi3.itphone_put_ringmode, tapi3if/ITPhone::put_RingMode
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
 - ITPhone::put_RingMode
 - tapi3if/ITPhone::put_RingMode
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
 - ITPhone.put_RingMode
---

# ITPhone::put_RingMode


## -description

The 
<b>put_RingMode</b> method requests that the phone change its ring mode.

The application must call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails.

## -parameters

### -param lRingMode [in]

Ring mode.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_ringmode">get_RingMode</a>