---
UID: NN:mfmediaengine.IMFMediaSourceExtensionNotify
title: IMFMediaSourceExtensionNotify
author: windows-sdk-content
description: Provides functionality for raising events associated with IMFMediaSourceExtension.
old-location: mf\imfmediasourceextensionnotify.htm
tech.root: medfound
ms.assetid: 44eed02d-cf92-41e5-8748-1ce11ab4aac0
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IMFMediaSourceExtensionNotify, IMFMediaSourceExtensionNotify interface [Media Foundation], IMFMediaSourceExtensionNotify interface [Media Foundation],described, mf.imfmediasourceextensionnotify, mfmediaengine/IMFMediaSourceExtensionNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - IMFMediaSourceExtensionNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSourceExtensionNotify interface


## -description


Provides functionality for raising events associated with <a href="https://msdn.microsoft.com/2acabcc2-242d-4b3d-b5b4-680c7973201f">IMFMediaSourceExtension</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSourceExtensionNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaSourceExtensionNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSourceExtensionNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4199b4e-320f-47ec-8434-862fb1c1db8d">OnSourceClose</a>
</td>
<td align="left" width="63%">
Used to indicate that the media source has closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ce65194-fb52-41e7-9ca4-d1e65fbbbeb0">OnSourceEnded</a>
</td>
<td align="left" width="63%">
Used to indicate that the media source has ended.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45120acf-48e1-4b4a-af50-f6052acdb533">OnSourceOpen</a>
</td>
<td align="left" width="63%">
Used to indicate that the  media source has opened.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

