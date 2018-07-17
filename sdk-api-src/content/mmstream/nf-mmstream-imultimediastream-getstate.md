---
UID: NF:mmstream.IMultiMediaStream.GetState
title: IMultiMediaStream::GetState
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The GetState method retrieves the current state of the multimedia stream object.
old-location: dshow\imultimediastream_getstate.htm
old-project: DirectShow
ms.assetid: 8d01c4cf-2de9-4e9c-8b6e-921284f4f1b6
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetState, GetState method [DirectShow], GetState method [DirectShow],IMultiMediaStream interface, IMultiMediaStream interface [DirectShow],GetState method, IMultiMediaStream.GetState, IMultiMediaStream::GetState, IMultiMediaStreamGetState, dshow.imultimediastream_getstate, mmstream/IMultiMediaStream::GetState
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IMultiMediaStream.GetState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMultiMediaStream::GetState


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetState</code> method retrieves the current state of the multimedia stream object.




## -parameters




### -param pCurrentState [out]

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/0be95819-0a42-4459-a891-194aacd26e2e">STREAM_STATE</a> enumeration.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8be6c74f-9290-48b4-ad66-8d7d7cc94174">IMultiMediaStream Interface</a>
 

 

