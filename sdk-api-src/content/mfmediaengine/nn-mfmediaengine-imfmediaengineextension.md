---
UID: NN:mfmediaengine.IMFMediaEngineExtension
title: IMFMediaEngineExtension
author: windows-sdk-content
description: Enables an application to load media resources in the Media Engine.
old-location: mf\imfmediaengineextension.htm
tech.root: medfound
ms.assetid: A032E0D0-2201-4B81-9FE0-8E9CE2707FDB
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMFMediaEngineExtension, IMFMediaEngineExtension interface [Media Foundation], IMFMediaEngineExtension interface [Media Foundation],described, mf.imfmediaengineextension, mfmediaengine/IMFMediaEngineExtension
ms.prod: windows
ms.technology: windows-sdk
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
 - IMFMediaEngineExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineExtension interface


## -description


Enables an application to load media resources in the Media Engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineExtension</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaEngineExtension</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineExtension</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/804E9F16-E4C9-41F6-8913-950A569FB835">BeginCreateObject</a>
</td>
<td align="left" width="63%">
Begins an asynchronous request to create either a byte stream or a media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E2FEC865-221E-41B5-8271-32A53D60619E">CancelObjectCreation</a>
</td>
<td align="left" width="63%">
Cancels the current request to create an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F715B4CB-363E-4EF2-962C-C0AFB26B088E">CanPlayType</a>
</td>
<td align="left" width="63%">
Queries whether the object can load a specified type of media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F2B19870-7529-4C8C-9FE6-B312F6A2D2ED">EndCreateObject</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to create a byte stream or media source.

</td>
</tr>
</table> 


## -remarks



To use this interface, set the <a href="https://msdn.microsoft.com/D2F3F41D-086A-4DEB-99D0-07574BC8F0D7">MF_MEDIA_ENGINE_EXTENSION</a> attribute when you call the <a href="https://msdn.microsoft.com/EDEAD2C4-5695-4E63-9E9E-B09D75B60B7F">IMFMediaEngineClassFactory::CreateInstance</a> method.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

