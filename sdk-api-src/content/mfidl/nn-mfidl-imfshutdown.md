---
UID: NN:mfidl.IMFShutdown
title: IMFShutdown
author: windows-sdk-content
description: Exposed by some Media Foundation objects that must be explicitly shut down.
old-location: mf\imfshutdown.htm
tech.root: medfound
ms.assetid: c3052658-51bb-401b-8db9-3428868899d6
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IMFShutdown, IMFShutdown interface [Media Foundation], IMFShutdown interface [Media Foundation],described, c3052658-51bb-401b-8db9-3428868899d6, mf.imfshutdown, mfidl/IMFShutdown
ms.prod: windows
ms.technology: windows-sdk
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
 - IMFShutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFShutdown interface


## -description


Exposed by some Media Foundation objects that must be explicitly shut down.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFShutdown</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFShutdown</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFShutdown</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8cf5f5f3-a3ad-4745-87e8-764ed118477a">GetShutdownStatus</a>
</td>
<td align="left" width="63%">
Queries the status of a prior call to the <a href="https://msdn.microsoft.com/9e7824d2-0f76-4c4c-98c5-ba51cd297de7">Shutdown</a> method.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e7824d2-0f76-4c4c-98c5-ba51cd297de7">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down a Media Foundation object and releases all resources associated with the object.
        

</td>
</tr>
</table> 


## -remarks



The following types of object expose <b>IMFShutdown</b>:

<ul>
<li>Content enablers (<a href="https://msdn.microsoft.com/45d02bd0-1104-47ec-8559-8cc51590fc62">IMFContentEnabler</a> interface)
          </li>
<li>Input trust authorities (<a href="https://msdn.microsoft.com/637e0225-6fd8-4b83-b4fb-119e7a5ef5d2">IMFInputTrustAuthority</a> interface)
          </li>
<li>Presentation clocks (<a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a> interface)
          </li>
<li>
<a href="https://msdn.microsoft.com/d438ffae-fc50-454f-8ce4-2d6676500fff">Asynchronous MFTs</a>
</li>
</ul>
Any component that creates one of these objects is responsible for calling <a href="https://msdn.microsoft.com/9e7824d2-0f76-4c4c-98c5-ba51cd297de7">Shutdown</a> on the object before releasing the object. Typically, applications do not create any of these objects directly, so it is not usually necessary to use this interface in an application.
      

To obtain a pointer to this interface, call <b>QueryInterface</b> on the object.
      

If you are implementing a custom object, your object can expose this interface, but only if you can guarantee that your application will call <a href="https://msdn.microsoft.com/9e7824d2-0f76-4c4c-98c5-ba51cd297de7">Shutdown</a>. 

Media sources, media sinks, and <i>synchronous</i> MFTs should not implement this interface, because the Media Foundation pipeline will not call <a href="https://msdn.microsoft.com/9e7824d2-0f76-4c4c-98c5-ba51cd297de7">Shutdown</a> on these objects.
      Asynchronous MFTs must implement this interface.

This interface is not related to the <a href="https://msdn.microsoft.com/10be2361-b5b4-4c10-92a1-527ca22c74e4">MFShutdown</a> function, which shuts down the Media Foundation platform, as described in <a href="https://msdn.microsoft.com/e4db81d3-7a9e-47d7-8611-6dac8026259c">Initializing Media Foundation</a>.
      

Some Media Foundation interfaces define a <b>Shutdown</b> method, which serves the same purpose as <a href="https://msdn.microsoft.com/9e7824d2-0f76-4c4c-98c5-ba51cd297de7">IMFShutdown::Shutdown</a> but is not directly related to it.
      




## -see-also




<a href="https://msdn.microsoft.com/a7dc3d4a-f21e-4af8-bee0-2d5f2cf28587">MFShutdownObject</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

