---
UID: NN:mfreadwrite.IMFSinkWriterCallback2
title: IMFSinkWriterCallback2 (mfreadwrite.h)
description: Extends the IMFSinkWriterCallback interface.
helpviewer_keywords: ["IMFSinkWriterCallback2","IMFSinkWriterCallback2 interface [Media Foundation]","IMFSinkWriterCallback2 interface [Media Foundation]","described","mf.imfsinkwritercallback2","mfreadwrite/IMFSinkWriterCallback2"]
old-location: mf\imfsinkwritercallback2.htm
tech.root: mf
ms.assetid: 92885A3C-137D-42DD-A65D-D2CE56A69A68
ms.date: 12/05/2018
ms.keywords: IMFSinkWriterCallback2, IMFSinkWriterCallback2 interface [Media Foundation], IMFSinkWriterCallback2 interface [Media Foundation],described, mf.imfsinkwritercallback2, mfreadwrite/IMFSinkWriterCallback2
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
 - IMFSinkWriterCallback2
 - mfreadwrite/IMFSinkWriterCallback2
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
 - IMFSinkWriterCallback2
---

# IMFSinkWriterCallback2 interface


## -description

Extends the <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback">IMFSinkWriterCallback</a> interface.

## -inheritance

The <b>IMFSinkWriterCallback2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSinkWriterCallback2</b> also has these types of members:

## -remarks

This interface provides a mechanism for apps that use <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a> to receive asynchronous notifications when the transform chain is complete and the system is ready for use or when an asynchronous error occurs.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
