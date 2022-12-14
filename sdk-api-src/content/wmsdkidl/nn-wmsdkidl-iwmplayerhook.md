---
UID: NN:wmsdkidl.IWMPlayerHook
title: IWMPlayerHook (wmsdkidl.h)
description: The IWMPlayerHook interface can be implemented by a player application that uses DirectX Video Acceleration (DirectX VA).
helpviewer_keywords: ["IWMPlayerHook","IWMPlayerHook interface [windows Media Format]","IWMPlayerHook interface [windows Media Format]","described","IWMPlayerHookInterface","wmformat.iwmplayerhook","wmsdkidl/IWMPlayerHook"]
old-location: wmformat\iwmplayerhook.htm
tech.root: wmformat
ms.assetid: 5e58cb6a-3398-4b12-881e-76f936f6c7b3
ms.date: 12/05/2018
ms.keywords: IWMPlayerHook, IWMPlayerHook interface [windows Media Format], IWMPlayerHook interface [windows Media Format],described, IWMPlayerHookInterface, wmformat.iwmplayerhook, wmsdkidl/IWMPlayerHook
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IWMPlayerHook
 - wmsdkidl/IWMPlayerHook
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMPlayerHook
---

# IWMPlayerHook interface


## -description

The <b>IWMPlayerHook</b> interface can be implemented by a player application that uses DirectX Video Acceleration (DirectX VA). This interface enables application-specific processing to be performed when samples from a video stream are passed to the DirectX VA enabled video card for decompression.

## -inheritance

The <b>IWMPlayerHook</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPlayerHook</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To assign an implementation of the <b>IWMPlayerHook</b> interface to an output in the reader object, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced5-setplayerhook">IWMReaderAdvanced5::SetPlayerHook</a>.

## -see-also

<a href="/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
