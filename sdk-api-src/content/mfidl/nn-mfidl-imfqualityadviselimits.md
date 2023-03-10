---
UID: NN:mfidl.IMFQualityAdviseLimits
title: IMFQualityAdviseLimits (mfidl.h)
description: Queries an object for the number of quality modes it supports.
helpviewer_keywords: ["IMFQualityAdviseLimits","IMFQualityAdviseLimits interface [Media Foundation]","IMFQualityAdviseLimits interface [Media Foundation]","described","mf.imfqualityadviselimits","mfidl/IMFQualityAdviseLimits"]
old-location: mf\imfqualityadviselimits.htm
tech.root: mf
ms.assetid: 8ef7088c-2f49-4be9-b719-481616e1737d
ms.date: 12/05/2018
ms.keywords: IMFQualityAdviseLimits, IMFQualityAdviseLimits interface [Media Foundation], IMFQualityAdviseLimits interface [Media Foundation],described, mf.imfqualityadviselimits, mfidl/IMFQualityAdviseLimits
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
 - IMFQualityAdviseLimits
 - mfidl/IMFQualityAdviseLimits
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
 - IMFQualityAdviseLimits
---

# IMFQualityAdviseLimits interface


## -description

Queries an object for the number of <i>quality modes</i> it supports. Quality modes are used to adjust the trade-off between quality and speed when rendering audio or video.

The default presenter for the <i>enhanced video renderer</i> (EVR) implements this interface. The EVR uses the interface to respond to quality messages from the quality manager.

## -inheritance

The <b>IMFQualityAdviseLimits</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFQualityAdviseLimits</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
