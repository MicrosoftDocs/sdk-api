---
UID: NN:mfmediaengine.IMFMediaEngineSrcElements
title: IMFMediaEngineSrcElements (mfmediaengine.h)
author: windows-sdk-content
description: Provides the Media Engine with a list of media resources.
old-location: mf\imfmediaenginesrcelements.htm
tech.root: medfound
ms.assetid: 37A3EAC0-639C-47F3-AAB9-588EBEC8E1E3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineSrcElements, IMFMediaEngineSrcElements interface [Media Foundation], IMFMediaEngineSrcElements interface [Media Foundation],described, mf.imfmediaenginesrcelements, mfmediaengine/IMFMediaEngineSrcElements
ms.topic: interface
req.header: mfmediaengine.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineSrcElements
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineSrcElements interface


## -description


Provides the Media Engine with a list of media resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineSrcElements</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaEngineSrcElements</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineSrcElements</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2C98A70B-F6B3-4CA7-8D04-958DFCCD2A50">AddElement</a>
</td>
<td align="left" width="63%">
Adds a source element to the end of the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/212883A5-5613-4BCC-8713-9CD5E6480136">GetLength</a>
</td>
<td align="left" width="63%">
Gets the number of source elements in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AC99D8D0-ACA6-4FE9-A061-1D3A7D92E596">GetMedia</a>
</td>
<td align="left" width="63%">
Gets the intended media type of an element in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7B788160-A342-48B4-A3F9-42F3BB83A24D">GetType</a>
</td>
<td align="left" width="63%">
Gets the MIME type of an element in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5935BE0D-0E5A-46A8-944C-096746C5FCA3">GetURL</a>
</td>
<td align="left" width="63%">
Gets the URL of an element in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4E867439-CBBA-4D36-9E0F-9034D3803688">RemoveAllElements</a>
</td>
<td align="left" width="63%">
Removes all of the source elements from the list.

</td>
</tr>
</table> 


## -remarks



The <b>IMFMediaEngineSrcElements</b> interface represents an ordered list of media resources.

This interface enables the application to provide the same audio/video content in several different encoding formats, such as H.264 and Windows Media Video. If a particular codec is not present on the user's computer, the Media Engine will try the next URL in the list. To use this interface, do the following:

<ol>
<li>Create an implementation of this interface.</li>
<li>Initialize your implementation with a list of URLs. Optionally, provide MIME types and media query strings for each URL.</li>
<li>Call the <a href="https://msdn.microsoft.com/7B1A1C43-A9BD-4DBF-B6A7-53BF9295CDAC">IMFMediaEngine::SetSourceElements</a> method.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

