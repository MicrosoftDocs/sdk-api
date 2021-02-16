---
UID: NF:dshowasf.IConfigAsfWriter2.StreamNumFromPin
title: IConfigAsfWriter2::StreamNumFromPin (dshowasf.h)
description: The StreamNumFromPin method retrieves the stream number associated with the specified input pin.
helpviewer_keywords: ["IConfigAsfWriter2 interface [DirectShow]","StreamNumFromPin method","IConfigAsfWriter2.StreamNumFromPin","IConfigAsfWriter2::StreamNumFromPin","IConfigAsfWriter2StreamNumFromPin","StreamNumFromPin","StreamNumFromPin method [DirectShow]","StreamNumFromPin method [DirectShow]","IConfigAsfWriter2 interface","dshow.iconfigasfwriter2_streamnumfrompin","dshowasf/IConfigAsfWriter2::StreamNumFromPin"]
old-location: dshow\iconfigasfwriter2_streamnumfrompin.htm
tech.root: dshow
ms.assetid: 374331ec-6665-4ed9-b4ee-6d33b1e2ef2c
ms.date: 12/05/2018
ms.keywords: IConfigAsfWriter2 interface [DirectShow],StreamNumFromPin method, IConfigAsfWriter2.StreamNumFromPin, IConfigAsfWriter2::StreamNumFromPin, IConfigAsfWriter2StreamNumFromPin, StreamNumFromPin, StreamNumFromPin method [DirectShow], StreamNumFromPin method [DirectShow],IConfigAsfWriter2 interface, dshow.iconfigasfwriter2_streamnumfrompin, dshowasf/IConfigAsfWriter2::StreamNumFromPin
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IConfigAsfWriter2::StreamNumFromPin
 - dshowasf/IConfigAsfWriter2::StreamNumFromPin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IConfigAsfWriter2.StreamNumFromPin
---

# IConfigAsfWriter2::StreamNumFromPin


## -description

The <code>StreamNumFromPin</code> method retrieves the stream number associated with the specified input pin.

## -parameters

### -param pPin [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface on the input pin.

### -param pwStreamNum [out]

Receives the stream number.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

You may need to use the Windows Media Format SDK interfaces directly to manipulate a stream before running the filter graph. This method is provided because you cannot assume that an ASF stream number is the same as the DirectShow pin number.

## -see-also

<a href="/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2">IConfigAsfWriter2 Interface</a>