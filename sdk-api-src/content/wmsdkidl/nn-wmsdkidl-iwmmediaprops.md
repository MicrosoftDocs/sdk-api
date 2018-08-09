---
UID: NN:wmsdkidl.IWMMediaProps
title: IWMMediaProps
author: windows-sdk-content
description: The IWMMediaProps interface sets and retrieves the WM_MEDIA_TYPE structure for an input, stream, or output.In the case of inputs and streams, the contents of the media type structure determine what actions the writer object will perform on the input data when writing the file. Typically, the input media type is an uncompressed type and the stream is a compressed type, so that the contents of their respective media type structures will determine the settings passed by the writer to the codec that will compress the stream.In the case of outputs, the media type structure determines the settings used to decompress the contents of a stream. The Windows Media codecs are capable of delivering output content in a variety of formats.The methods of IWMMediaProps are inherited by IWMVideoMediaProps, which provides access to additional settings for specifying video media types. The methods are also inherited by IWMInputMediaProps and IWMOutputMediaProps.An instance of the IWMMediaProps interface exists for every stream configuration object, input media properties object, and output media properties object. You can retrieve a pointer to this interface by calling the QueryInterface method of any other interface in one of those objects.
old-location: wmformat\iwmmediaprops.htm
old-project: wmformat
ms.assetid: a81abd80-e487-421c-ba81-9b43c4233084
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMMediaProps, IWMMediaProps interface [windows Media Format], IWMMediaProps interface [windows Media Format],described, IWMMediaPropsInterface, wmformat.iwmmediaprops, wmsdkidl/IWMMediaProps
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMMediaProps interface


## -description



The <b>IWMMediaProps</b> interface sets and retrieves the <a href="https://msdn.microsoft.com/37a9ac59-e152-47e1-96ee-b816cd645936">WM_MEDIA_TYPE</a> structure for an input, stream, or output.

In the case of inputs and streams, the contents of the media type structure determine what actions the writer object will perform on the input data when writing the file. Typically, the input media type is an uncompressed type and the stream is a compressed type, so that the contents of their respective media type structures will determine the settings passed by the writer to the codec that will compress the stream.

In the case of outputs, the media type structure determines the settings used to decompress the contents of a stream. The Windows Media codecs are capable of delivering output content in a variety of formats.

The methods of <b>IWMMediaProps</b> are inherited by <a href="https://msdn.microsoft.com/4d6ba1d8-b046-450b-a3f9-4810faba5b77">IWMVideoMediaProps</a>, which provides access to additional settings for specifying video media types. The methods are also inherited by <a href="https://msdn.microsoft.com/d901ac66-d4b3-4256-bd7b-53cccb3de644">IWMInputMediaProps</a> and <a href="https://msdn.microsoft.com/8cf40db5-3902-4c14-b728-98da90567e89">IWMOutputMediaProps</a>.

An instance of the <b>IWMMediaProps</b> interface exists for every stream configuration object, input media properties object, and output media properties object. You can retrieve a pointer to this interface by calling the <b>QueryInterface</b> method of any other interface in one of those objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMMediaProps</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMMediaProps</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8357e5c6-d8c6-4a30-8446-85fa7fa118f7">GetMediaType</a>
</td>
<td align="left" width="63%">
Retrieves a <b>WM_MEDIA_TYPE</b> structure describing the media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the major type of the media (audio, video, or script).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a89bf24-6b76-4645-8f39-f1979029d67e">SetMediaType</a>
</td>
<td align="left" width="63%">
Specifies a <b>WM_MEDIA_TYPE</b> structure describing the media type.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the <b>QueryInterface</b> method of this interface, see the topic for the object on which this interface is implemented.



## -see-also




<a href="https://msdn.microsoft.com/e7aa6c99-b6b3-4e5b-869d-3387f70dad87">Input Media Properties Object</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/96fa7c66-59a0-4eb3-ace4-a827b139f978">Output Media Properties Object</a>



<a href="https://msdn.microsoft.com/228e334c-9d9b-4604-a225-73af7af3255f">Stream Configuration Object</a>
 

 

