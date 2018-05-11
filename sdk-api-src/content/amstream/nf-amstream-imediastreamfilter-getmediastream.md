---
UID: NF:amstream.IMediaStreamFilter.GetMediaStream
title: IMediaStreamFilter::GetMediaStream
author: windows-driver-content
description: Note  This interface is deprecated. New applications should not use it. The GetMediaStream method retrieves a media stream, specified by purpose ID.
old-location: dshow\imediastreamfilter_getmediastream.htm
old-project: DirectShow
ms.assetid: 27ef63cf-36a4-4d35-bd38-3c51b1343ee1
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetMediaStream, GetMediaStream method [DirectShow], GetMediaStream method [DirectShow],IMediaStreamFilter interface, IMediaStreamFilter interface [DirectShow],GetMediaStream method, IMediaStreamFilter.GetMediaStream, IMediaStreamFilter::GetMediaStream, IMediaStreamFilterGetMediaStream, amstream/IMediaStreamFilter::GetMediaStream, dshow.imediastreamfilter_getmediastream
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
req.typenames: AMSI_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	amstream.h
api_name:
-	IMediaStreamFilter.GetMediaStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMediaStreamFilter::GetMediaStream


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetMediaStream</code> method retrieves a media stream, specified by purpose ID.




## -parameters




### -param idPurpose [in]

Reference to an <a href="https://msdn.microsoft.com/83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf">MSPID</a> value that specifies which stream to retrieve.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_NOSTREAM</b></dt>
</dl>
</td>
<td width="60%">
No matching stream was found.

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
 

 

