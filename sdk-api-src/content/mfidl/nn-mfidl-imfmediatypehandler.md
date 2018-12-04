---
UID: NN:mfidl.IMFMediaTypeHandler
title: IMFMediaTypeHandler
author: windows-sdk-content
description: Gets and sets media types on an object, such as a media source or media sink.
old-location: mf\imfmediatypehandler.htm
tech.root: medfound
ms.assetid: 5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: 5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36, IMFMediaTypeHandler, IMFMediaTypeHandler interface [Media Foundation], IMFMediaTypeHandler interface [Media Foundation],described, mf.imfmediatypehandler, mfidl/IMFMediaTypeHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaTypeHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaTypeHandler interface


## -description


Gets and sets media types on an object, such as a media source or media sink.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaTypeHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaTypeHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaTypeHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1676e40-81a2-4311-bba6-528bfa45a708">GetCurrentMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the current media type of the object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1560d113-80a9-48bb-9f3d-6e3a288db962">GetMajorType</a>
</td>
<td align="left" width="63%">
Retrieves the major media type of the object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1827675-bbc4-45d8-8c6e-644b0d2addd4">GetMediaTypeByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a media type from the object's list of supported media types.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5ee41bc-ee8b-4990-ae9d-92ef54597f31">GetMediaTypeCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of media types in the object's list of supported media types.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea52defa-8b78-4f40-97ae-ed6a5ee4849e">IsMediaTypeSupported</a>
</td>
<td align="left" width="63%">
Queries whether the object supports a specified media type.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7f69adb-2a4a-47a9-bb92-ad9d005b962f">RemoteGetCurrentMediaType</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://msdn.microsoft.com/b1676e40-81a2-4311-bba6-528bfa45a708">GetCurrentMediaType</a>. (Not used by applications.)
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77ff397e-4fa8-4849-98b8-6bdd035c0e89">SetCurrentMediaType</a>
</td>
<td align="left" width="63%">
Sets the object media type.
        

</td>
</tr>
</table> 


## -remarks



This interface is exposed by <i>media-type handlers</i>.

<ul>
<li> For media sources, get the media-type handler from the stream descriptor by calling <a href="https://msdn.microsoft.com/8e991417-fe15-4749-94c4-26c621692b52">IMFStreamDescriptor::GetMediaTypeHandler</a>.</li>
<li>For media sinks, get the media-type handler by calling <a href="https://msdn.microsoft.com/819d06b1-6b52-4496-bed8-a08b8f0b6153">IMFStreamSink::GetMediaTypeHandler</a>.</li>
</ul>
If you are implementing a custom media source or media sink, you can create a simple media-type handler by calling <a href="https://msdn.microsoft.com/441bd03d-b314-4f26-ad67-e6997e5edc9d">MFCreateSimpleTypeHandler</a>, or you can provide your own implementation.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>



<a href="https://msdn.microsoft.com/714c8bda-5ce1-47e2-ba73-9304e26b3129">Presentation Descriptors</a>
 

 

