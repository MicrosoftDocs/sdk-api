---
UID: NF:mfidl.IMFByteStreamCacheControl2.IsBackgroundTransferActive
title: IMFByteStreamCacheControl2::IsBackgroundTransferActive (mfidl.h)
description: Queries whether background transfer is active.
helpviewer_keywords: ["IMFByteStreamCacheControl2 interface [Media Foundation]","IsBackgroundTransferActive method","IMFByteStreamCacheControl2.IsBackgroundTransferActive","IMFByteStreamCacheControl2::IsBackgroundTransferActive","IsBackgroundTransferActive","IsBackgroundTransferActive method [Media Foundation]","IsBackgroundTransferActive method [Media Foundation]","IMFByteStreamCacheControl2 interface","mf.imfbytestreamcachecontrol2_isbackgroundtransferactive","mfidl/IMFByteStreamCacheControl2::IsBackgroundTransferActive"]
old-location: mf\imfbytestreamcachecontrol2_isbackgroundtransferactive.htm
tech.root: mf
ms.assetid: FC08E5E8-A7E0-461C-B70C-B1273FCDD1A0
ms.date: 12/05/2018
ms.keywords: IMFByteStreamCacheControl2 interface [Media Foundation],IsBackgroundTransferActive method, IMFByteStreamCacheControl2.IsBackgroundTransferActive, IMFByteStreamCacheControl2::IsBackgroundTransferActive, IsBackgroundTransferActive, IsBackgroundTransferActive method [Media Foundation], IsBackgroundTransferActive method [Media Foundation],IMFByteStreamCacheControl2 interface, mf.imfbytestreamcachecontrol2_isbackgroundtransferactive, mfidl/IMFByteStreamCacheControl2::IsBackgroundTransferActive
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFByteStreamCacheControl2::IsBackgroundTransferActive
 - mfidl/IMFByteStreamCacheControl2::IsBackgroundTransferActive
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFByteStreamCacheControl2.IsBackgroundTransferActive
---

# IMFByteStreamCacheControl2::IsBackgroundTransferActive


## -description

Queries whether background transfer is active.

## -parameters

### -param pfActive [out]

Receives the value <b>TRUE</b> if background transfer is currently active, or <b>FALSE</b> otherwise.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Background transfer might stop because the cache limit was reached (see <a href="/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamcachecontrol2-setcachelimit">IMFByteStreamCacheControl2::SetCacheLimit</a>) or because the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamcachecontrol-stopbackgroundtransfer">IMFByteStreamCacheControl::StopBackgroundTransfer</a> method was called.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol2">IMFByteStreamCacheControl2</a>