---
UID: NF:tapi3if.ITPhone.get_RingVolume
title: ITPhone::get_RingVolume (tapi3if.h)
description: The get_RingVolume method retrieves the current ring volume for the phone.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","get_RingVolume method","ITPhone.get_RingVolume","ITPhone::get_RingVolume","_tapi3_itphone_get_ringvolume","get_RingVolume","get_RingVolume method [TAPI 2.2]","get_RingVolume method [TAPI 2.2]","ITPhone interface","tapi3.itphone_get_ringvolume","tapi3if/ITPhone::get_RingVolume"]
old-location: tapi3\itphone_get_ringvolume.htm
tech.root: tapi3
ms.assetid: 147553f1-74a7-4f80-bbf3-b140d9b375ba
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_RingVolume method, ITPhone.get_RingVolume, ITPhone::get_RingVolume, _tapi3_itphone_get_ringvolume, get_RingVolume, get_RingVolume method [TAPI 2.2], get_RingVolume method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_ringvolume, tapi3if/ITPhone::get_RingVolume
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
 - ITPhone::get_RingVolume
 - tapi3if/ITPhone::get_RingVolume
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
 - ITPhone.get_RingVolume
---

# ITPhone::get_RingVolume


## -description

The 
<b>get_RingVolume</b> method retrieves the current ring volume for the phone.

The application must call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails.

## -parameters

### -param plRingVolume [out]

Ring volume.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-put_ringvolume">put_RingVolume</a>