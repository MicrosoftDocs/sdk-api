---
UID: NN:mfreadwrite.IMFSourceReaderCallback2
title: IMFSourceReaderCallback2
author: windows-sdk-content
description: Extends the IMFSourceReaderCallback interface.
old-location: mf\imfsourcereadercallback2.htm
tech.root: medfound
ms.assetid: D0EC7FE9-74C3-4A7C-A5F3-798A3D6EF2CC
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IMFSourceReaderCallback2, IMFSourceReaderCallback2 interface [Media Foundation], IMFSourceReaderCallback2 interface [Media Foundation],described, mf.imfsourcereadercallback2, mfreadwrite/IMFSourceReaderCallback2
ms.prod: windows
ms.technology: windows-sdk
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
 - IMFSourceReaderCallback2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSourceReaderCallback2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/fff8b6e6-5d56-4301-b3ce-f3ff49398593">IMFSourceReaderCallback</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceReaderCallback2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSourceReaderCallback2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSourceReaderCallback2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9239DE9E-8CC3-493A-B7FE-AB0294907069">OnStreamError</a>
</td>
<td align="left" width="63%">
Called when an asynchronous error occurs with the <a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84A4154C-574C-4B78-A83B-2EE036C0A68D">OnTransformChange</a>
</td>
<td align="left" width="63%">
Called when the transform chain in the <a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a> is built or modified.

</td>
</tr>
</table> 


## -remarks



This interface provides a mechanism for apps that use <a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a> to receive asynchronous notifications when the transform chain is complete and the system is ready for use or when an asynchronous error occurs.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

