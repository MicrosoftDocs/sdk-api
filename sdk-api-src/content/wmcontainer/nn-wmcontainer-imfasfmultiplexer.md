---
UID: NN:wmcontainer.IMFASFMultiplexer
title: IMFASFMultiplexer (wmcontainer.h)
description: Provides methods to create Advanced Systems Format (ASF) data packets.
helpviewer_keywords: ["IMFASFMultiplexer","IMFASFMultiplexer interface [Media Foundation]","IMFASFMultiplexer interface [Media Foundation]","described","bdb549b5-425b-4f77-b413-723ceb7acd11","mf.imfasfmultiplexer","wmcontainer/IMFASFMultiplexer"]
old-location: mf\imfasfmultiplexer.htm
tech.root: mf
ms.assetid: bdb549b5-425b-4f77-b413-723ceb7acd11
ms.date: 12/05/2018
ms.keywords: IMFASFMultiplexer, IMFASFMultiplexer interface [Media Foundation], IMFASFMultiplexer interface [Media Foundation],described, bdb549b5-425b-4f77-b413-723ceb7acd11, mf.imfasfmultiplexer, wmcontainer/IMFASFMultiplexer
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFMultiplexer
 - wmcontainer/IMFASFMultiplexer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFMultiplexer
---

# IMFASFMultiplexer interface


## -description

Provides methods to create Advanced Systems Format (ASF) data packets. The methods of this interface process input samples into the packets that make up an ASF data section. The ASF multiplexer exposes this interface. To create the ASF multiplexer, call <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer">MFCreateASFMultiplexer</a>.

## -inheritance

The <b>IMFASFMultiplexer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFASFMultiplexer</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/asf-multiplexer">ASF Multiplexer</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
