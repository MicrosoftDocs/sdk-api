---
UID: NN:mfmediaengine.IMFMediaEngineSrcElements
title: IMFMediaEngineSrcElements (mfmediaengine.h)
description: Provides the Media Engine with a list of media resources.helpviewer_keywords: ["IMFMediaEngineSrcElements","IMFMediaEngineSrcElements interface [Media Foundation]","IMFMediaEngineSrcElements interface [Media Foundation]","described","mf.imfmediaenginesrcelements","mfmediaengine/IMFMediaEngineSrcElements"]
old-location: mf\imfmediaenginesrcelements.htm
tech.root: medfound
ms.assetid: 37A3EAC0-639C-47F3-AAB9-588EBEC8E1E3
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineSrcElements, IMFMediaEngineSrcElements interface [Media Foundation], IMFMediaEngineSrcElements interface [Media Foundation],described, mf.imfmediaenginesrcelements, mfmediaengine/IMFMediaEngineSrcElements
f1_keywords:
- mfmediaengine/IMFMediaEngineSrcElements
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineSrcElements interface


## -description


Provides the Media Engine with a list of media resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineSrcElements</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngineSrcElements</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesrcelements-addelement">AddElement</a>
</td>
<td align="left" width="63%">
Adds a source element to the end of the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesrcelements-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the number of source elements in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesrcelements-getmedia">GetMedia</a>
</td>
<td align="left" width="63%">
Gets the intended media type of an element in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesrcelements-gettype">GetType</a>
</td>
<td align="left" width="63%">
Gets the MIME type of an element in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesrcelements-geturl">GetURL</a>
</td>
<td align="left" width="63%">
Gets the URL of an element in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesrcelements-removeallelements">RemoveAllElements</a>
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
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsourceelements">IMFMediaEngine::SetSourceElements</a> method.</li>
</ol>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

