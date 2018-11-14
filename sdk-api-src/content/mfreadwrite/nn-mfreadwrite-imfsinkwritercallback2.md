---
UID: NN:mfreadwrite.IMFSinkWriterCallback2
title: IMFSinkWriterCallback2
author: windows-sdk-content
description: Extends the IMFSinkWriterCallback interface.
old-location: mf\imfsinkwritercallback2.htm
tech.root: medfound
ms.assetid: 92885A3C-137D-42DD-A65D-D2CE56A69A68
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFSinkWriterCallback2, IMFSinkWriterCallback2 interface [Media Foundation], IMFSinkWriterCallback2 interface [Media Foundation],described, mf.imfsinkwritercallback2, mfreadwrite/IMFSinkWriterCallback2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - mfreadwrite.h
api_name:
 - IMFSinkWriterCallback2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSinkWriterCallback2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/fa0295e6-473d-4304-9a7b-24584cade0a0">IMFSinkWriterCallback</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSinkWriterCallback2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSinkWriterCallback2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSinkWriterCallback2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31239998-9D12-46A4-B3F3-68167F6EFFDD">OnStreamError</a>
</td>
<td align="left" width="63%">
Called when an asynchronous error occurs with the <a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A0D93B37-1A74-486E-8A7C-6D909E2F25FD">OnTransformChange</a>
</td>
<td align="left" width="63%">
Called when the transform chain in the <a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a> is built or modified.

</td>
</tr>
</table> 


## -remarks



This interface provides a mechanism for apps that use <a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a> to receive asynchronous notifications when the transform chain is complete and the system is ready for use or when an asynchronous error occurs.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

