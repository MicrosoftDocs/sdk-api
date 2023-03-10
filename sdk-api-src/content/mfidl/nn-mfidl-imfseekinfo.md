---
UID: NN:mfidl.IMFSeekInfo
title: IMFSeekInfo (mfidl.h)
description: For a particular seek position, gets the two nearest key frames. (IMFSeekInfo)
helpviewer_keywords: ["IMFSeekInfo","IMFSeekInfo interface [Media Foundation]","IMFSeekInfo interface [Media Foundation]","described","mf.imfseekinfo","mfidl/IMFSeekInfo"]
old-location: mf\imfseekinfo.htm
tech.root: mf
ms.assetid: 5B1AD3A1-D5ED-4F9D-A895-0312E6EB3072
ms.date: 12/05/2018
ms.keywords: IMFSeekInfo, IMFSeekInfo interface [Media Foundation], IMFSeekInfo interface [Media Foundation],described, mf.imfseekinfo, mfidl/IMFSeekInfo
req.header: mfidl.h
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
 - IMFSeekInfo
 - mfidl/IMFSeekInfo
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
 - IMFSeekInfo
---

# IMFSeekInfo interface


## -description

For a particular seek position, gets the two nearest key frames.

## -inheritance

The <b>IMFSeekInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSeekInfo</b> also has these types of members:

## -remarks

A media source can implement this interface as an optional service. To get a pointer to the interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfgetservice">IMFGetService::GetService</a> with the service identifier <b>MF_SCRUBBING_SERVICE</b>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
