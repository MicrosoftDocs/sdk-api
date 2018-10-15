---
UID: NN:mfmediaengine.IMFBufferListNotify
title: IMFBufferListNotify
author: windows-sdk-content
description: Enables IMFSourceBufferList object to notify its clients of important state changes.
old-location: mf\imfbufferlistnotify.htm
tech.root: medfound
ms.assetid: 2a2705b4-fac3-4059-b2c9-c03efaa9c15e
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IMFBufferListNotify, IMFBufferListNotify interface [Media Foundation], IMFBufferListNotify interface [Media Foundation],described, mf.imfbufferlistnotify, mfmediaengine/IMFBufferListNotify
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
 - IMFBufferListNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFBufferListNotify interface


## -description


Enables <a href="https://msdn.microsoft.com/26f66c2d-5f84-485f-bc86-c8399666c9f1">IMFSourceBufferList</a> object to notify its clients of important state changes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFBufferListNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFBufferListNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFBufferListNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94b943d7-b67a-4f35-b5a6-2e89b4018ff3">OnAddSourceBuffer</a>
</td>
<td align="left" width="63%">
Indicates that a <a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a> has been added.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b203ba3-d5b8-4ab9-ae3e-74c289d74749">OnRemoveSourceBuffer</a>
</td>
<td align="left" width="63%">
Indicates that a <a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a> has been removed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

