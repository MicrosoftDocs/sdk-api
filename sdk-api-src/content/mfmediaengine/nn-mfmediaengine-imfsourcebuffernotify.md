---
UID: NN:mfmediaengine.IMFSourceBufferNotify
title: IMFSourceBufferNotify
author: windows-sdk-content
description: Provides functionality for raising events associated with IMFSourceBuffer.
old-location: mf\imfsourcebuffernotify.htm
tech.root: medfound
ms.assetid: 4a823d37-f55a-4810-aaed-4e04f5371d3b
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFSourceBufferNotify, IMFSourceBufferNotify interface [Media Foundation], IMFSourceBufferNotify interface [Media Foundation],described, mf.imfsourcebuffernotify, mfmediaengine/IMFSourceBufferNotify
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
 - IMFSourceBufferNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSourceBufferNotify interface


## -description


Provides functionality for raising events associated with <a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceBufferNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSourceBufferNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSourceBufferNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65d8bbb3-e683-4a9d-acb2-023932d3e44d">OnAbort</a>
</td>
<td align="left" width="63%">
Used to indicate that the source buffer has been aborted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7187b7a-0090-4380-82bb-a7f72d54232e">OnError</a>
</td>
<td align="left" width="63%">
Used to indicate that an error has occurred with the  source buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c41f50f-7f0b-4676-9522-3866aedab047">OnUpdate</a>
</td>
<td align="left" width="63%">
Used to indicate that the source buffer is updating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a06d5765-d91e-4cbc-ac12-09d1ce4d84f6">OnUpdateEnd</a>
</td>
<td align="left" width="63%">
Used to indicate that the source buffer has finished updating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/513ef55d-756e-4ae3-b312-6a4178bc2f42">OnUpdateStart</a>
</td>
<td align="left" width="63%">
Used to indicate that the source buffer has started updating.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

