---
UID: NN:mfidl.IMFClock
title: IMFClock (mfidl.h)
description: Provides timing information from a clock in Microsoft Media Foundation.
helpviewer_keywords: ["3a60bfec-8511-4a84-a833-e0c73c593970","IMFClock","IMFClock interface [Media Foundation]","IMFClock interface [Media Foundation]","described","mf.imfclock","mfidl/IMFClock"]
old-location: mf\imfclock.htm
tech.root: mf
ms.assetid: 3a60bfec-8511-4a84-a833-e0c73c593970
ms.date: 12/05/2018
ms.keywords: 3a60bfec-8511-4a84-a833-e0c73c593970, IMFClock, IMFClock interface [Media Foundation], IMFClock interface [Media Foundation],described, mf.imfclock, mfidl/IMFClock
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFClock
 - mfidl/IMFClock
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
 - IMFClock
---

# IMFClock interface


## -description

Provides timing information from a clock in Microsoft Media Foundation.

Clocks and some media sinks expose this interface through <b>QueryInterface</b>.

## -inheritance

The <b>IMFClock</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFClock</b> also has these types of members:

## -remarks

The <b>IMFClock</b> interface applies to any kind of clock. The presentation clock exposes the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a> interface in addition to <b>IMFClock</b>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>
