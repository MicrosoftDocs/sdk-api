---
UID: NN:mfmediaengine.IMFMediaEngineClassFactory
title: IMFMediaEngineClassFactory
author: windows-sdk-content
description: Creates an instance of the Media Engine.
old-location: mf\imfmediaengineclassfactory.htm
tech.root: medfound
ms.assetid: 8E4E84A0-BCFC-4CBF-813B-4FEE2B42A83E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFMediaEngineClassFactory, IMFMediaEngineClassFactory interface [Media Foundation], IMFMediaEngineClassFactory interface [Media Foundation],described, mf.imfmediaengineclassfactory, mfmediaengine/IMFMediaEngineClassFactory
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
 - IMFMediaEngineClassFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineClassFactory interface


## -description


Creates an instance of the Media Engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineClassFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaEngineClassFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineClassFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C089473D-CD35-4F5D-8C78-EDE0FA8C13EB">CreateError</a>
</td>
<td align="left" width="63%">
Creates a media error object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EDEAD2C4-5695-4E63-9E9E-B09D75B60B7F">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates a new instance of the Media Engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/293769E8-8C8A-40D1-AF51-1DBB773F88D5">CreateTimeRange</a>
</td>
<td align="left" width="63%">
Creates a time range object.

</td>
</tr>
</table> 


## -remarks



Before using this interface, call <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> and <a href="https://msdn.microsoft.com/b4472e40-3681-4b26-9385-4df7bf19c2d8">MFStartup</a>.

To get a pointer to this interface, call <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a>. The class identifier is <b>CLSID_MFMediaEngineClassFactory</b>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=241429">Media Engine Sample</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

