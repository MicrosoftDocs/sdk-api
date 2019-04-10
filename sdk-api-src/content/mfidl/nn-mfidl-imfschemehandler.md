---
UID: NN:mfidl.IMFSchemeHandler
title: IMFSchemeHandler (mfidl.h)
author: windows-sdk-content
description: Creates a media source or a byte stream from a URL.
old-location: mf\imfschemehandler.htm
tech.root: medfound
ms.assetid: a342054e-2cb5-494a-a2f7-d144c72d1fa5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFSchemeHandler, IMFSchemeHandler interface [Media Foundation], IMFSchemeHandler interface [Media Foundation],described, a342054e-2cb5-494a-a2f7-d144c72d1fa5, mf.imfschemehandler, mfidl/IMFSchemeHandler
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
 - IMFSchemeHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSchemeHandler interface


## -description


Creates a media source or a byte stream from a URL.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSchemeHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSchemeHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSchemeHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78858e8c-0eb3-4b62-84f0-76e9dff0e3ce">BeginCreateObject</a>
</td>
<td align="left" width="63%">
Begins an asynchronous request to create an object from a URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/662a4c47-95f8-4a84-ab2b-96e51d13906c">CancelObjectCreation</a>
</td>
<td align="left" width="63%">
Cancels the current request to create an object from a URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3f88904-c30f-4d40-ac79-c83b0a06f1fa">EndCreateObject</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to create an object from a URL.

</td>
</tr>
</table> 


## -remarks



Applications do not use this interface. This interface is exposed by scheme handlers, which are used by the source resolver. A scheme handler is designed to parse one type of URL scheme. When the scheme handler is given a URL, it parses the resource that is located at that URL and creates either a media source or a byte stream.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>
 

 

