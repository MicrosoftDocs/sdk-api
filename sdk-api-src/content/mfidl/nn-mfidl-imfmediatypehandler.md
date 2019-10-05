---
UID: NN:mfidl.IMFMediaTypeHandler
title: IMFMediaTypeHandler (mfidl.h)
author: windows-sdk-content
description: Gets and sets media types on an object, such as a media source or media sink.
old-location: mf\imfmediatypehandler.htm
tech.root: medfound
ms.assetid: 5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36, IMFMediaTypeHandler, IMFMediaTypeHandler interface [Media Foundation], IMFMediaTypeHandler interface [Media Foundation],described, mf.imfmediatypehandler, mfidl/IMFMediaTypeHandler
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFMediaTypeHandler"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaTypeHandler interface


## -description


Gets and sets media types on an object, such as a media source or media sink.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaTypeHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaTypeHandler</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype">GetCurrentMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the current media type of the object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype">GetMajorType</a>
</td>
<td align="left" width="63%">
Retrieves the major media type of the object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex">GetMediaTypeByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a media type from the object's list of supported media types.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount">GetMediaTypeCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of media types in the object's list of supported media types.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported">IsMediaTypeSupported</a>
</td>
<td align="left" width="63%">
Queries whether the object supports a specified media type.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/remotegetcurrentmediatype">RemoteGetCurrentMediaType</a>
</td>
<td align="left" width="63%">
Remotable version of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype">GetCurrentMediaType</a>. (Not used by applications.)
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype">SetCurrentMediaType</a>
</td>
<td align="left" width="63%">
Sets the object media type.
        

</td>
</tr>
</table> 


## -remarks



This interface is exposed by <i>media-type handlers</i>.

<ul>
<li> For media sources, get the media-type handler from the stream descriptor by calling <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler">IMFStreamDescriptor::GetMediaTypeHandler</a>.</li>
<li>For media sinks, get the media-type handler by calling <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-getmediatypehandler">IMFStreamSink::GetMediaTypeHandler</a>.</li>
</ul>
If you are implementing a custom media source or media sink, you can create a simple media-type handler by calling <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatesimpletypehandler">MFCreateSimpleTypeHandler</a>, or you can provide your own implementation.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-types">Media Types</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/presentation-descriptors">Presentation Descriptors</a>
 

 

