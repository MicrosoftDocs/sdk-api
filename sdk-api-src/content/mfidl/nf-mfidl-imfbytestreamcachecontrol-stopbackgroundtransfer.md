---
UID: NF:mfidl.IMFByteStreamCacheControl.StopBackgroundTransfer
title: IMFByteStreamCacheControl::StopBackgroundTransfer (mfidl.h)
description: Stops the background transfer of data to the local cache.
helpviewer_keywords: ["IMFByteStreamCacheControl interface [Media Foundation]","StopBackgroundTransfer method","IMFByteStreamCacheControl.StopBackgroundTransfer","IMFByteStreamCacheControl::StopBackgroundTransfer","StopBackgroundTransfer","StopBackgroundTransfer method [Media Foundation]","StopBackgroundTransfer method [Media Foundation]","IMFByteStreamCacheControl interface","mf.imfbytestreamcachecontrol_stopbackgroundtransfer","mfidl/IMFByteStreamCacheControl::StopBackgroundTransfer"]
old-location: mf\imfbytestreamcachecontrol_stopbackgroundtransfer.htm
tech.root: mf
ms.assetid: 9f0f7102-c839-4e92-a798-5ea31ceba013
ms.date: 12/05/2018
ms.keywords: IMFByteStreamCacheControl interface [Media Foundation],StopBackgroundTransfer method, IMFByteStreamCacheControl.StopBackgroundTransfer, IMFByteStreamCacheControl::StopBackgroundTransfer, StopBackgroundTransfer, StopBackgroundTransfer method [Media Foundation], StopBackgroundTransfer method [Media Foundation],IMFByteStreamCacheControl interface, mf.imfbytestreamcachecontrol_stopbackgroundtransfer, mfidl/IMFByteStreamCacheControl::StopBackgroundTransfer
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IMFByteStreamCacheControl::StopBackgroundTransfer
 - mfidl/IMFByteStreamCacheControl::StopBackgroundTransfer
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
 - IMFByteStreamCacheControl.StopBackgroundTransfer
---

# IMFByteStreamCacheControl::StopBackgroundTransfer


## -description

Stops the background transfer of data to the local cache.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The byte stream resumes transferring data to the cache if the application does one of the following:

<ul>
<li>Reads data from the byte stream.</li>
<li>Calls the byte stream's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfbytestreambuffering-enablebuffering">IMFByteStreamBuffering::EnableBuffering</a> method.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol">IMFByteStreamCacheControl</a>
