---
UID: NN:wmsdkidl.IWMMediaProps
title: IWMMediaProps (wmsdkidl.h)
description: The IWMMediaProps interface sets and retrieves the WM_MEDIA_TYPE structure for an input, stream, or output.In the case of inputs and streams, the contents of the media type structure determine what actions the writer object will perform on the input data when writing the file. Typically, the input media type is an uncompressed type and the stream is a compressed type, so that the contents of their respective media type structures will determine the settings passed by the writer to the codec that will compress the stream.In the case of outputs, the media type structure determines the settings used to decompress the contents of a stream. The Windows Media codecs are capable of delivering output content in a variety of formats.The methods of IWMMediaProps are inherited by IWMVideoMediaProps, which provides access to additional settings for specifying video media types. The methods are also inherited by IWMInputMediaProps and IWMOutputMediaProps.An instance of the IWMMediaProps interface exists for every stream configuration object, input media properties object, and output media properties object. You can retrieve a pointer to this interface by calling the QueryInterface method of any other interface in one of those objects.
helpviewer_keywords: ["IWMMediaProps","IWMMediaProps interface [windows Media Format]","IWMMediaProps interface [windows Media Format]","described","IWMMediaPropsInterface","wmformat.iwmmediaprops","wmsdkidl/IWMMediaProps"]
old-location: wmformat\iwmmediaprops.htm
tech.root: wmformat
ms.assetid: a81abd80-e487-421c-ba81-9b43c4233084
ms.date: 4/26/2023
ms.keywords: IWMMediaProps, IWMMediaProps interface [windows Media Format], IWMMediaProps interface [windows Media Format],described, IWMMediaPropsInterface, wmformat.iwmmediaprops, wmsdkidl/IWMMediaProps
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
 - IWMMediaProps
 - wmsdkidl/IWMMediaProps
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
 - IWMMediaProps
---

# IWMMediaProps interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMMediaProps</b> interface sets and retrieves the <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type">WM_MEDIA_TYPE</a> structure for an input, stream, or output.

In the case of inputs and streams, the contents of the media type structure determine what actions the writer object will perform on the input data when writing the file. Typically, the input media type is an uncompressed type and the stream is a compressed type, so that the contents of their respective media type structures will determine the settings passed by the writer to the codec that will compress the stream.

In the case of outputs, the media type structure determines the settings used to decompress the contents of a stream. The Windows Media codecs are capable of delivering output content in a variety of formats.

The methods of <b>IWMMediaProps</b> are inherited by <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmvideomediaprops">IWMVideoMediaProps</a>, which provides access to additional settings for specifying video media types. The methods are also inherited by <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops">IWMInputMediaProps</a> and <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps</a>.

An instance of the <b>IWMMediaProps</b> interface exists for every stream configuration object, input media properties object, and output media properties object. You can retrieve a pointer to this interface by calling the <b>QueryInterface</b> method of any other interface in one of those objects.

## -inheritance

The <b>IWMMediaProps</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMMediaProps</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/input-media-properties-object">Input Media Properties Object</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/output-media-properties-object">Output Media Properties Object</a>



<a href="/windows/desktop/wmformat/stream-configuration-object">Stream Configuration Object</a>
