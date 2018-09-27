---
UID: NF:amstream.IMediaStreamFilter.EnumMediaStreams
title: IMediaStreamFilter::EnumMediaStreams
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The EnumMediaStreams method retrieves a media stream, specified by index.
old-location: dshow\imediastreamfilter_enummediastreams.htm
tech.root: DirectShow
ms.assetid: 5f62abda-6192-4adb-985d-9bffe310b407
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: EnumMediaStreams, EnumMediaStreams method [DirectShow], EnumMediaStreams method [DirectShow],IMediaStreamFilter interface, IMediaStreamFilter interface [DirectShow],EnumMediaStreams method, IMediaStreamFilter.EnumMediaStreams, IMediaStreamFilter::EnumMediaStreams, IMediaStreamFilterEnumMediaStreams, amstream/IMediaStreamFilter::EnumMediaStreams, dshow.imediastreamfilter_enummediastreams
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amstream.h
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
 - amstream.h
api_name:
 - IMediaStreamFilter.EnumMediaStreams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaStreamFilter::EnumMediaStreams


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>EnumMediaStreams</code> method retrieves a media stream, specified by index.




## -parameters




### -param Index [in]

Index of the media stream to retrieve.


### -param ppMediaStream [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream</a> interface pointer.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



If the method succeeds, the caller must release the <b>IMediaStream</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/1ac4976b-7088-47ac-9689-58c143746f05">IMediaStreamFilter Interface</a>
 

 

