---
UID: NN:strmif.IMpeg2Demultiplexer
title: IMpeg2Demultiplexer (strmif.h)
description: This interface is implemented on the MPEG-2 Demultiplexer filter (Demux) and is used in both program stream mode and transport stream mode.
helpviewer_keywords: ["IMpeg2Demultiplexer","IMpeg2Demultiplexer interface [DirectShow]","IMpeg2Demultiplexer interface [DirectShow]","described","IMpeg2DemultiplexerInterface","dshow.impeg2demultiplexer","strmif/IMpeg2Demultiplexer"]
old-location: dshow\impeg2demultiplexer.htm
tech.root: dshow
ms.assetid: e9242b96-0fc3-428e-b7ee-91a4f5e67305
ms.date: 12/05/2018
ms.keywords: IMpeg2Demultiplexer, IMpeg2Demultiplexer interface [DirectShow], IMpeg2Demultiplexer interface [DirectShow],described, IMpeg2DemultiplexerInterface, dshow.impeg2demultiplexer, strmif/IMpeg2Demultiplexer
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMpeg2Demultiplexer
 - strmif/IMpeg2Demultiplexer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMpeg2Demultiplexer
---

# IMpeg2Demultiplexer interface


## -description

This interface is implemented on the <a href="/windows/desktop/DirectShow/mpeg-2-demultiplexer">MPEG-2 Demultiplexer</a> filter (Demux) and is used in both program stream mode and transport stream mode. It is called by applications or other filters to create, configure and delete output pins on the Demux. This interface is not exposed when the filter is playing back a file (pull-mode).

## -inheritance

The <b>IMpeg2Demultiplexer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMpeg2Demultiplexer</b> also has these types of members:

