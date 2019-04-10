---
UID: NN:strmif.IResourceConsumer
title: IResourceConsumer (strmif.h)
author: windows-sdk-content
description: The IResourceConsumer interface provides a callback mechanism for objects using the IResourceManager interface.An object must implement IResourceConsumer if it uses the IResourceManager interface to request resources from the filter graph manager.
old-location: dshow\iresourceconsumer.htm
tech.root: DirectShow
ms.assetid: dda2b207-dcd8-42df-95a3-d4bfbb4a7fd8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IResourceConsumer, IResourceConsumer interface [DirectShow], IResourceConsumer interface [DirectShow],described, IResourceConsumerInterface, dshow.iresourceconsumer, strmif/IResourceConsumer
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IResourceConsumer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResourceConsumer interface


## -description



The <code>IResourceConsumer</code> interface provides a callback mechanism for objects using the <a href="https://msdn.microsoft.com/8cbe908e-5675-4134-81e7-2c5c31b0ffc5">IResourceManager</a> interface.

An object must implement <code>IResourceConsumer</code> if it uses the <a href="https://msdn.microsoft.com/8cbe908e-5675-4134-81e7-2c5c31b0ffc5">IResourceManager</a> interface to request resources from the filter graph manager. The filter graph manager calls methods on <code>IResourceConsumer</code> to notify the object when a resource becomes available, or when the object should release a resource that it acquired.

Applications typically do not use or implement this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResourceConsumer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IResourceConsumer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IResourceConsumer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e88d90af-681e-483b-9b29-9844eec75e41">AcquireResource</a>
</td>
<td align="left" width="63%">
Notifies the resource consumer that a resource might be acquired.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f0a5830-dcaa-4020-9e78-0cbe64e13360">ReleaseResource</a>
</td>
<td align="left" width="63%">
Requests the resource consumer to release the specified resource.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8cbe908e-5675-4134-81e7-2c5c31b0ffc5">IResourceManager Interface</a>
 

 

