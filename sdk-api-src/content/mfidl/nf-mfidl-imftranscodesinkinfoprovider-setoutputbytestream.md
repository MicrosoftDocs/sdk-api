---
UID: NF:mfidl.IMFTranscodeSinkInfoProvider.SetOutputByteStream
title: IMFTranscodeSinkInfoProvider::SetOutputByteStream (mfidl.h)
description: Sets an output byte stream for the transcode media sink.
helpviewer_keywords: ["IMFTranscodeSinkInfoProvider interface [Media Foundation]","SetOutputByteStream method","IMFTranscodeSinkInfoProvider.SetOutputByteStream","IMFTranscodeSinkInfoProvider::SetOutputByteStream","SetOutputByteStream","SetOutputByteStream method [Media Foundation]","SetOutputByteStream method [Media Foundation]","IMFTranscodeSinkInfoProvider interface","mf.imftranscodesinkinfoprovider_setoutputbytestream","mfidl/IMFTranscodeSinkInfoProvider::SetOutputByteStream"]
old-location: mf\imftranscodesinkinfoprovider_setoutputbytestream.htm
tech.root: mf
ms.assetid: 234bed82-a148-4313-a8cb-eefe2061b7ed
ms.date: 12/05/2018
ms.keywords: IMFTranscodeSinkInfoProvider interface [Media Foundation],SetOutputByteStream method, IMFTranscodeSinkInfoProvider.SetOutputByteStream, IMFTranscodeSinkInfoProvider::SetOutputByteStream, SetOutputByteStream, SetOutputByteStream method [Media Foundation], SetOutputByteStream method [Media Foundation],IMFTranscodeSinkInfoProvider interface, mf.imftranscodesinkinfoprovider_setoutputbytestream, mfidl/IMFTranscodeSinkInfoProvider::SetOutputByteStream
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IMFTranscodeSinkInfoProvider::SetOutputByteStream
 - mfidl/IMFTranscodeSinkInfoProvider::SetOutputByteStream
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
 - IMFTranscodeSinkInfoProvider.SetOutputByteStream
---

# IMFTranscodeSinkInfoProvider::SetOutputByteStream


## -description

Sets an output byte stream for the transcode media sink.

## -parameters

### -param pByteStreamActivate [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface of a byte-stream activation object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method to provide a writable byte stream 
        that will receive the transcoded data.

Alternatively, you can provide the name of an  output file, by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imftranscodesinkinfoprovider-setoutputfile">IMFTranscodeSinkInfoProvider::SetOutputFile</a>. These two methods are mutually exclusive.

The <i>pByteStreamActivate</i> parameter must specify an activation object that creates a writable byte stream. Internally, the transcode media sink calls <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> to create the byte stream, as follows:


``` syntax
IMFByteStream *pByteStream = NULL;

HRESULT hr = pByteStreamActivate->ActivateObject(IID_IMFByteStream, (void**)&pByteStream);
```

Currently, Microsoft Media Foundation does not provide any byte-stream activation objects. To use this method, an application must provide a custom implementation of <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodesinkinfoprovider">IMFTranscodeSinkInfoProvider</a>
