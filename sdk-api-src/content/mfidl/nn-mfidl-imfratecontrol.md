---
UID: NN:mfidl.IMFRateControl
title: IMFRateControl (mfidl.h)
description: Gets or sets the playback rate.
helpviewer_keywords: ["54303c32-b260-4364-9130-a592694f2816","IMFRateControl","IMFRateControl interface [Media Foundation]","IMFRateControl interface [Media Foundation]","described","mf.imfratecontrol","mfidl/IMFRateControl"]
old-location: mf\imfratecontrol.htm
tech.root: mf
ms.assetid: 54303c32-b260-4364-9130-a592694f2816
ms.date: 12/05/2018
ms.keywords: 54303c32-b260-4364-9130-a592694f2816, IMFRateControl, IMFRateControl interface [Media Foundation], IMFRateControl interface [Media Foundation],described, mf.imfratecontrol, mfidl/IMFRateControl
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
 - IMFRateControl
 - mfidl/IMFRateControl
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
 - IMFRateControl
---

# IMFRateControl interface


## -description

Gets or sets the playback rate.

## -inheritance

The <b>IMFRateControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFRateControl</b> also has these types of members:

## -remarks

Objects can expose this interface as a service. To obtain a pointer to the interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> with the service identifier MF_RATE_CONTROL_SERVICE. The Media Session supports this interface. Media sources and transforms support this interface if they support rate changes. Media sinks do not need to support this interface. Media sinks are notified of rate changes through the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate">IMFClockStateSink::OnClockSetRate</a> method.

For more information, see <a href="/windows/desktop/medfound/about-rate-control">About Rate Control</a>.

To discover the playback rates that an object supports, use the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport">IMFRateSupport</a> interface

## -see-also

<a href="/windows/desktop/medfound/about-rate-control">About Rate Control</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
