---
UID: NN:mfidl.IMFRateSupport
title: IMFRateSupport (mfidl.h)
description: Queries the range of playback rates that are supported, including reverse playback.
helpviewer_keywords: ["IMFRateSupport","IMFRateSupport interface [Media Foundation]","IMFRateSupport interface [Media Foundation]","described","a6c495fa-0f6a-4e4c-8fba-996b22d55053","mf.imfratesupport","mfidl/IMFRateSupport"]
old-location: mf\imfratesupport.htm
tech.root: mf
ms.assetid: a6c495fa-0f6a-4e4c-8fba-996b22d55053
ms.date: 12/05/2018
ms.keywords: IMFRateSupport, IMFRateSupport interface [Media Foundation], IMFRateSupport interface [Media Foundation],described, a6c495fa-0f6a-4e4c-8fba-996b22d55053, mf.imfratesupport, mfidl/IMFRateSupport
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
 - IMFRateSupport
 - mfidl/IMFRateSupport
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
 - IMFRateSupport
---

# IMFRateSupport interface


## -description

Queries the range of playback rates that are supported, including reverse playback.

To get a pointer to this interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> with the service identifier MF_RATE_CONTROL_SERVICE.

## -inheritance

The <b>IMFRateSupport</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFRateSupport</b> also has these types of members:

## -remarks

Applications can use this interface to discover the fastest and slowest playback rates that are possible, and to query whether a given playback rate is supported. Applications obtain this interface from the Media Session. Internally, the Media Session queries the objects in the pipeline. For more information, see <a href="/windows/desktop/medfound/how-to-determine-supported-rates">How to Determine Supported Rates</a>.

To get the current playback rate and to change the playback rate, use the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol">IMFRateControl</a> interface.

Playback rates are expressed as a ratio the normal playback rate. Reverse playback is expressed as a negative rate. Playback is either <i>thinned</i> or <i>non-thinned</i>. In thinned playback, some of the source data is skipped (typically delta frames). In non-thinned playback, all of the source data is rendered.

You might need to implement this interface if you are writing a pipeline object (media source, transform, or media sink). For more information, see <a href="/windows/desktop/medfound/implementing-rate-control">Implementing Rate Control</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol">IMFRateControl</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
