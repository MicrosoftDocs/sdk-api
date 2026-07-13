---
UID: NN:mfidl.IMFShutdown
title: IMFShutdown (mfidl.h)
description: Exposed by some Media Foundation objects that must be explicitly shut down.
helpviewer_keywords: ["IMFShutdown","IMFShutdown interface [Media Foundation]","IMFShutdown interface [Media Foundation]","described","c3052658-51bb-401b-8db9-3428868899d6","mf.imfshutdown","mfidl/IMFShutdown"]
old-location: mf\imfshutdown.htm
tech.root: mf
ms.assetid: c3052658-51bb-401b-8db9-3428868899d6
ms.date: 12/05/2018
ms.keywords: IMFShutdown, IMFShutdown interface [Media Foundation], IMFShutdown interface [Media Foundation],described, c3052658-51bb-401b-8db9-3428868899d6, mf.imfshutdown, mfidl/IMFShutdown
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
 - IMFShutdown
 - mfidl/IMFShutdown
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
 - IMFShutdown
---

# IMFShutdown interface


## -description

Exposed by some Media Foundation objects that must be explicitly shut down.

## -inheritance

The <b>IMFShutdown</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFShutdown</b> also has these types of members:

## -remarks

The following types of object expose <b>IMFShutdown</b>:

<ul>
<li>Content enablers (<a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler">IMFContentEnabler</a> interface)
          </li>
<li>Input trust authorities (<a href="/windows/desktop/api/mfidl/nn-mfidl-imfinputtrustauthority">IMFInputTrustAuthority</a> interface)
          </li>
<li>Presentation clocks (<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a> interface)
          </li>
<li>
<a href="/windows/desktop/medfound/asynchronous-mfts">Asynchronous MFTs</a>
</li>
</ul>
Any component that creates one of these objects is responsible for calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown">Shutdown</a> on the object before releasing the object. Typically, applications do not create any of these objects directly, so it is not usually necessary to use this interface in an application.
      

To obtain a pointer to this interface, call <b>QueryInterface</b> on the object.
      

If you are implementing a custom object, your object can expose this interface, but only if you can guarantee that your application will call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown">Shutdown</a>. 

Media sources, media sinks, and <i>synchronous</i> MFTs should not implement this interface, because the Media Foundation pipeline will not call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown">Shutdown</a> on these objects.
      Asynchronous MFTs must implement this interface.

This interface is not related to the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a> function, which shuts down the Media Foundation platform, as described in <a href="/windows/desktop/medfound/initializing-media-foundation">Initializing Media Foundation</a>.
      

Some Media Foundation interfaces define a <b>Shutdown</b> method, which serves the same purpose as <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown">IMFShutdown::Shutdown</a> but is not directly related to it.

## -see-also

<a href="/windows/desktop/api/mfidl/nf-mfidl-mfshutdownobject">MFShutdownObject</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
