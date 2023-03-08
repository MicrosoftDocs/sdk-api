---
UID: NF:tapi3if.ITPhone.put_RingVolume
title: ITPhone::put_RingVolume (tapi3if.h)
description: The put_RingVolume method requests that the phone change its ring volume.
helpviewer_keywords: ["ITPhone interface [TAPI 2.2]","put_RingVolume method","ITPhone.put_RingVolume","ITPhone::put_RingVolume","_tapi3_itphone_put_ringvolume","put_RingVolume","put_RingVolume method [TAPI 2.2]","put_RingVolume method [TAPI 2.2]","ITPhone interface","tapi3.itphone_put_ringvolume","tapi3if/ITPhone::put_RingVolume"]
old-location: tapi3\itphone_put_ringvolume.htm
tech.root: tapi3
ms.assetid: 858ca6a8-a53b-4858-b4b0-985230ec8ea0
ms.date: 12/05/2018
ms.keywords: ITPhone interface [TAPI 2.2],put_RingVolume method, ITPhone.put_RingVolume, ITPhone::put_RingVolume, _tapi3_itphone_put_ringvolume, put_RingVolume, put_RingVolume method [TAPI 2.2], put_RingVolume method [TAPI 2.2],ITPhone interface, tapi3.itphone_put_ringvolume, tapi3if/ITPhone::put_RingVolume
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
 - ITPhone::put_RingVolume
 - tapi3if/ITPhone::put_RingVolume
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
 - ITPhone.put_RingVolume
---

# ITPhone::put_RingVolume


## -description

The 
<b>put_RingVolume</b> method requests that the phone change its ring volume.

The application must call 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-open">ITPhone::Open</a> before invoking this method; otherwise, the invocation fails.

## -parameters

### -param lRingVolume [in]

Phone volume. For more information, see the following Remarks section.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the phone is currently ringing (RingMode != 0), the new volume takes effect immediately. If the phone is not currently ringing (RingMode == 0), the new volume takes effect the next time the phone rings.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-get_ringvolume">get_RingVolume</a>