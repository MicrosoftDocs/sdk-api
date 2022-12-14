---
UID: NF:mfreadwrite.IMFSinkWriterEx.GetTransformForStream
title: IMFSinkWriterEx::GetTransformForStream (mfreadwrite.h)
description: Gets a pointer to a Media Foundation transform (MFT) for a specified stream. (IMFSinkWriterEx.GetTransformForStream)
helpviewer_keywords: ["GetTransformForStream","GetTransformForStream method [Media Foundation]","GetTransformForStream method [Media Foundation]","IMFSinkWriterEx interface","IMFSinkWriterEx interface [Media Foundation]","GetTransformForStream method","IMFSinkWriterEx.GetTransformForStream","IMFSinkWriterEx::GetTransformForStream","mf.imfsinkwriterex_gettransformforstream","mfreadwrite/IMFSinkWriterEx::GetTransformForStream"]
old-location: mf\imfsinkwriterex_gettransformforstream.htm
tech.root: mf
ms.assetid: 72EEC01F-ED62-4DD7-A18C-766D01705CAE
ms.date: 12/05/2018
ms.keywords: GetTransformForStream, GetTransformForStream method [Media Foundation], GetTransformForStream method [Media Foundation],IMFSinkWriterEx interface, IMFSinkWriterEx interface [Media Foundation],GetTransformForStream method, IMFSinkWriterEx.GetTransformForStream, IMFSinkWriterEx::GetTransformForStream, mf.imfsinkwriterex_gettransformforstream, mfreadwrite/IMFSinkWriterEx::GetTransformForStream
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFSinkWriterEx::GetTransformForStream
 - mfreadwrite/IMFSinkWriterEx::GetTransformForStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSinkWriterEx.GetTransformForStream
---

# IMFSinkWriterEx::GetTransformForStream


## -description

Gets a pointer to a Media Foundation transform (MFT) for a specified stream.

## -parameters

### -param dwStreamIndex [in]

The zero-based index of a stream.

### -param dwTransformIndex [in]

The zero-based index of the MFT to retrieve.

### -param pGuidCategory [out]

Receives a pointer to a GUID that specifies the category of the MFT. For a list of possible values, see <a href="/windows/desktop/medfound/mft-category">MFT_CATEGORY</a>.

### -param ppTransform [out]

Receives a pointer to the <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> interface of the MFT. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex">IMFSinkWriterEx</a>
