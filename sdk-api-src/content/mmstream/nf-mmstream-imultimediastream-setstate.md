---
UID: NF:mmstream.IMultiMediaStream.SetState
title: IMultiMediaStream::SetState
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The SetState method runs or stops the multimedia stream object.
old-location: dshow\imultimediastream_setstate.htm
old-project: DirectShow
ms.assetid: 69c3612f-e91a-4ab3-8f6d-2966e64a9220
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IMultiMediaStream interface [DirectShow],SetState method, IMultiMediaStream.SetState, IMultiMediaStream::SetState, IMultiMediaStreamSetState, SetState, SetState method [DirectShow], SetState method [DirectShow],IMultiMediaStream interface, dshow.imultimediastream_setstate, mmstream/IMultiMediaStream::SetState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmstream.h
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
tech.root: 
req.typenames: STREAM_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mmstream.h
api_name:
-	IMultiMediaStream.SetState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMultiMediaStream::SetState


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetState</code> method runs or stops the multimedia stream object.




## -parameters




### -param NewState [in]

A member of the <a href="https://msdn.microsoft.com/0be95819-0a42-4459-a891-194aacd26e2e">STREAM_STATE</a> enumeration, specifying the new state (running or stopped).


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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



Stopping the multimedia stream object deletes any data that is pending.




## -see-also




<a href="https://msdn.microsoft.com/8be6c74f-9290-48b4-ad66-8d7d7cc94174">IMultiMediaStream Interface</a>
 

 

