---
UID: NN:mfreadwrite.IMFSourceReaderCallback2
title: IMFSourceReaderCallback2 (mfreadwrite.h)
description: Extends the IMFSourceReaderCallback interface.
helpviewer_keywords: ["IMFSourceReaderCallback2","IMFSourceReaderCallback2 interface [Media Foundation]","IMFSourceReaderCallback2 interface [Media Foundation]","described","mf.imfsourcereadercallback2","mfreadwrite/IMFSourceReaderCallback2"]
old-location: mf\imfsourcereadercallback2.htm
tech.root: mf
ms.assetid: D0EC7FE9-74C3-4A7C-A5F3-798A3D6EF2CC
ms.date: 12/05/2018
ms.keywords: IMFSourceReaderCallback2, IMFSourceReaderCallback2 interface [Media Foundation], IMFSourceReaderCallback2 interface [Media Foundation],described, mf.imfsourcereadercallback2, mfreadwrite/IMFSourceReaderCallback2
req.header: mfreadwrite.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSourceReaderCallback2
 - mfreadwrite/IMFSourceReaderCallback2
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
 - IMFSourceReaderCallback2
---

# IMFSourceReaderCallback2 interface


## -description

Extends the <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback">IMFSourceReaderCallback</a> interface.

## -inheritance

The <b>IMFSourceReaderCallback2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSourceReaderCallback2</b> also has these types of members:

## -remarks

This interface provides a mechanism for apps that use <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a> to receive asynchronous notifications when the transform chain is complete and the system is ready for use or when an asynchronous error occurs.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
