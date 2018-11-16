---
UID: NF:windows.media.streaming.IMediaRendererFactory.CreateMediaRendererAsync
title: IMediaRendererFactory::streaming
author: windows-sdk-content
description: Asynchronously creates a new instance of an object that implements the IMediaRenderer interface using the specified Unique Device Name (UDN).
old-location: mediastreaming\imediarendererfactory_createmediarendererasync.htm
tech.root: mediastreaming
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateMediaRendererAsync, CreateMediaRendererAsync method [Media Streaming API], CreateMediaRendererAsync method [Media Streaming API],IMediaRendererFactory interface, IMediaRendererFactory interface [Media Streaming API],CreateMediaRendererAsync method, IMediaRendererFactory.CreateMediaRendererAsync, IMediaRendererFactory.streaming, IMediaRendererFactory::CreateMediaRendererAsync, IMediaRendererFactory::streaming, mediastreaming.imediarendererfactory_createmediarendererasync, windows/IMediaRendererFactory::CreateMediaRendererAsync
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: windows.media.streaming.h
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
 - windows.media.streaming.h
api_name:
 - IMediaRendererFactory.CreateMediaRendererAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- windows.media.streaming.h
: 
- IMediaRendererFactory.CreateMediaRendererAsync
: 
---

# IMediaRendererFactory::streaming


## -description


Asynchronously creates a new instance of an object that implements the <a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a> interface using the specified Unique Device Name (UDN).


## -parameters




### -param deviceIdentifier [in]

An HSTRING containing a UDN that identifies the DLNA DMR device for which an instance of <a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a> will be created.


### -param value [out, retval]

Receives a reference to a <a href="https://msdn.microsoft.com/0BC87D9E-5285-4F98-96B4-C841DDECBBE0">CreateMediaRendererOperation</a> object that is used to get results from the asynchronous operation.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/E07EC208-CF00-46D0-B00D-AA8E59F12A0A">IMediaRendererFactory</a>
 

 

