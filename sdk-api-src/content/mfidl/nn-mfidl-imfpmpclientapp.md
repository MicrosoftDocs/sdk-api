---
UID: NN:mfidl.IMFPMPClientApp
title: IMFPMPClientApp
author: windows-sdk-content
description: Provides a mechanism for a media source to implement content protection functionality in a Windows Store apps.
old-location: mf\imfpmpclientapp.htm
tech.root: medfound
ms.assetid: 03cd9e3c-65ac-40ad-802d-e36127dbd61f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMFPMPClientApp, IMFPMPClientApp interface [Media Foundation], IMFPMPClientApp interface [Media Foundation],described, mf.imfpmpclientapp, mfidl/IMFPMPClientApp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
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
 - mfidl.h
api_name:
 - IMFPMPClientApp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFPMPClientApp interface


## -description


Provides a mechanism for a media source to implement content protection functionality in a Windows Store apps.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMPClientApp</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFPMPClientApp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPMPClientApp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8809e691-f0cf-4c1f-8409-5e7fbac46b16">SetPMPHost</a>
</td>
<td align="left" width="63%">
Initialize the component with <a href="https://msdn.microsoft.com/ca24930d-bd1e-4c12-8246-1e505a98944a">IMFPMPHostApp</a>.

</td>
</tr>
</table> 


## -remarks



<b>When to implement:</b> 
A media source implements <b>IMFPMPClientApp</b> in order to implement content protection functionality for Windows Store apps.






## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/CF3A427D-31D2-45FF-BE87-F192B758204E">PMP Media Session</a>



<a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>
 

 

