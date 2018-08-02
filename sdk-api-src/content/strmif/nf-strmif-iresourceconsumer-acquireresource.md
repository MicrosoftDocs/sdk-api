---
UID: NF:strmif.IResourceConsumer.AcquireResource
title: IResourceConsumer::AcquireResource
author: windows-sdk-content
description: The AcquireResource method notifies the resource consumer that a resource might be acquired.
old-location: dshow\iresourceconsumer_acquireresource.htm
old-project: DirectShow
ms.assetid: e88d90af-681e-483b-9b29-9844eec75e41
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: AcquireResource, AcquireResource method [DirectShow], AcquireResource method [DirectShow],IResourceConsumer interface, IResourceConsumer interface [DirectShow],AcquireResource method, IResourceConsumer.AcquireResource, IResourceConsumer::AcquireResource, IResourceConsumerAcquireResource, dshow.iresourceconsumer_acquireresource, strmif/IResourceConsumer::AcquireResource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IResourceConsumer.AcquireResource
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IResourceConsumer::AcquireResource


## -description



The <code>AcquireResource</code> method notifies the resource consumer that a resource might be acquired.




## -parameters




### -param idResource [in]

Resource identifier of the resource to be acquired.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Consumer has successfully acquired the resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Consumer has not acquired the resource but will use <a href="https://msdn.microsoft.com/a5c52f5b-1c21-4f4c-b698-15b6ec7f7fed">IResourceManager::NotifyAcquire</a> when it does.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_RESOURCE_NOT_NEEDED</b></dt>
</dl>
</td>
<td width="60%">
Consumer no longer needs the resource.

</td>
</tr>
</table>
 

The method may return some other error code, if the consumer fails to acquire the resource.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/dda2b207-dcd8-42df-95a3-d4bfbb4a7fd8">IResourceConsumer Interface</a>
 

 

