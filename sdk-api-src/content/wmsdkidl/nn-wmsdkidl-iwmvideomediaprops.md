---
UID: NN:wmsdkidl.IWMVideoMediaProps
title: IWMVideoMediaProps (wmsdkidl.h)
description: With this interface, the application can specify additional video-specific parameters not available on the IWMMediaProps interface.To get access to the methods of this interface, call QueryInterface on a stream configuration object.
helpviewer_keywords: ["IWMVideoMediaProps","IWMVideoMediaProps interface [windows Media Format]","IWMVideoMediaProps interface [windows Media Format]","described","IWMVideoMediaPropsInterface","wmformat.iwmvideomediaprops","wmsdkidl/IWMVideoMediaProps"]
old-location: wmformat\iwmvideomediaprops.htm
tech.root: wmformat
ms.assetid: 4d6ba1d8-b046-450b-a3f9-4810faba5b77
ms.date: 4/26/2023
ms.keywords: IWMVideoMediaProps, IWMVideoMediaProps interface [windows Media Format], IWMVideoMediaProps interface [windows Media Format],described, IWMVideoMediaPropsInterface, wmformat.iwmvideomediaprops, wmsdkidl/IWMVideoMediaProps
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
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
req.lib: Wmvcore.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMVideoMediaProps
 - wmsdkidl/IWMVideoMediaProps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
api_name:
 - IWMVideoMediaProps
---

# IWMVideoMediaProps interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

With this interface, the application can specify additional video-specific parameters not available on the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps</a> interface.

To get access to the methods of this interface, call <b>QueryInterface</b> on a stream configuration object. For more information, see <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig Interface</a>).

## -inheritance

The <b>IWMVideoMediaProps</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps</a>. <b>IWMVideoMediaProps</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
