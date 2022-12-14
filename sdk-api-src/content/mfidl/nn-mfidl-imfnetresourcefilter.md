---
UID: NN:mfidl.IMFNetResourceFilter
title: IMFNetResourceFilter (mfidl.h)
description: Notifies the application when a byte stream requests a URL, and enables the application to block URL redirection.
helpviewer_keywords: ["IMFNetResourceFilter","IMFNetResourceFilter interface [Media Foundation]","IMFNetResourceFilter interface [Media Foundation]","described","mf.imfnetresourcefilter","mfidl/IMFNetResourceFilter"]
old-location: mf\imfnetresourcefilter.htm
tech.root: mf
ms.assetid: AC8FBD93-B39B-4530-8475-275D3D0DA512
ms.date: 12/05/2018
ms.keywords: IMFNetResourceFilter, IMFNetResourceFilter interface [Media Foundation], IMFNetResourceFilter interface [Media Foundation],described, mf.imfnetresourcefilter, mfidl/IMFNetResourceFilter
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IMFNetResourceFilter
 - mfidl/IMFNetResourceFilter
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
 - IMFNetResourceFilter
---

# IMFNetResourceFilter interface


## -description

Notifies the application when a byte stream requests a URL, and enables the application to block URL redirection.

## -inheritance

The <b>IMFNetResourceFilter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFNetResourceFilter</b> also has these types of members:

## -remarks

To set the callback interface:

<ol>
<li>Query the byte stream object for the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface.</li>
<li>Call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown">IMFAttributes::SetUnknown</a> to set the <a href="/windows/desktop/medfound/mfnetsource-resource-filter">MFNETSOURCE_RESOURCE_FILTER</a> attribute.</li>
</ol>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
