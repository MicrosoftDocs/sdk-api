---
UID: NN:mfidl.IMFTopoLoader
title: IMFTopoLoader (mfidl.h)
description: Converts a partial topology into a full topology.
helpviewer_keywords: ["5ebf117c-e60a-40f2-a24b-c4f9dbdae942","IMFTopoLoader","IMFTopoLoader interface [Media Foundation]","IMFTopoLoader interface [Media Foundation]","described","mf.imftopoloader","mfidl/IMFTopoLoader"]
old-location: mf\imftopoloader.htm
tech.root: mf
ms.assetid: 5ebf117c-e60a-40f2-a24b-c4f9dbdae942
ms.date: 12/05/2018
ms.keywords: 5ebf117c-e60a-40f2-a24b-c4f9dbdae942, IMFTopoLoader, IMFTopoLoader interface [Media Foundation], IMFTopoLoader interface [Media Foundation],described, mf.imftopoloader, mfidl/IMFTopoLoader
req.header: mfidl.h
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
 - IMFTopoLoader
 - mfidl/IMFTopoLoader
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
 - IMFTopoLoader
---

# IMFTopoLoader interface


## -description

Converts a partial topology into a full topology. The topology loader exposes this interface.

## -inheritance

The <b>IMFTopoLoader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTopoLoader</b> also has these types of members:

## -remarks

To create the topology loader, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader">MFCreateTopoLoader</a> function.

## -see-also

<a href="/windows/desktop/medfound/advanced-topology-building">Advanced Topology Building</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>
