---
UID: NN:wmsdkidl.IWMMediaProps
title: IWMMediaProps (wmsdkidl.h)
author: windows-sdk-content
description: The IWMMediaProps interface sets and retrieves the WM_MEDIA_TYPE structure for an input, stream, or output.In the case of inputs and streams, the contents of the media type structure determine what actions the writer object will perform on the input data when writing the file. Typically, the input media type is an uncompressed type and the stream is a compressed type, so that the contents of their respective media type structures will determine the settings passed by the writer to the codec that will compress the stream.In the case of outputs, the media type structure determines the settings used to decompress the contents of a stream. The Windows Media codecs are capable of delivering output content in a variety of formats.The methods of IWMMediaProps are inherited by IWMVideoMediaProps, which provides access to additional settings for specifying video media types. The methods are also inherited by IWMInputMediaProps and IWMOutputMediaProps.An instance of the IWMMediaProps interface exists for every stream configuration object, input media properties object, and output media properties object. You can retrieve a pointer to this interface by calling the QueryInterface method of any other interface in one of those objects.
old-location: wmformat\iwmmediaprops.htm
tech.root: wmformat
ms.assetid: a81abd80-e487-421c-ba81-9b43c4233084
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMMediaProps, IWMMediaProps interface [windows Media Format], IWMMediaProps interface [windows Media Format],described, IWMMediaPropsInterface, wmformat.iwmmediaprops, wmsdkidl/IWMMediaProps
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMMediaProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMMediaProps interface


## -description



The <b>IWMMediaProps</b> interface sets and retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/ns-wmsdkidl-_wmmediatype">WM_MEDIA_TYPE</a> structure for an input, stream, or output.

In the case of inputs and streams, the contents of the media type structure determine what actions the writer object will perform on the input data when writing the file. Typically, the input media type is an uncompressed type and the stream is a compressed type, so that the contents of their respective media type structures will determine the settings passed by the writer to the codec that will compress the stream.

In the case of outputs, the media type structure determines the settings used to decompress the contents of a stream. The Windows Media codecs are capable of delivering output content in a variety of formats.

The methods of <b>IWMMediaProps</b> are inherited by <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmvideomediaprops">IWMVideoMediaProps</a>, which provides access to additional settings for specifying video media types. The methods are also inherited by <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops">IWMInputMediaProps</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps</a>.

An instance of the <b>IWMMediaProps</b> interface exists for every stream configuration object, input media properties object, and output media properties object. You can retrieve a pointer to this interface by calling the <b>QueryInterface</b> method of any other interface in one of those objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMMediaProps</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMMediaProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMMediaProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype">GetMediaType</a>
</td>
<td align="left" width="63%">
Retrieves a <b>WM_MEDIA_TYPE</b> structure describing the media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the major type of the media (audio, video, or script).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmediaprops-setmediatype">SetMediaType</a>
</td>
<td align="left" width="63%">
Specifies a <b>WM_MEDIA_TYPE</b> structure describing the media type.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the <b>QueryInterface</b> method of this interface, see the topic for the object on which this interface is implemented.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/input-media-properties-object">Input Media Properties Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/output-media-properties-object">Output Media Properties Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/stream-configuration-object">Stream Configuration Object</a>
 

 

