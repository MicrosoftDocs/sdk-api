---
UID: NF:amstream.IAMMultiMediaStream.Initialize
title: IAMMultiMediaStream::Initialize
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The Initialize method initializes the multimedia stream object.
old-location: dshow\iammultimediastream_initialize.htm
tech.root: DirectShow
ms.assetid: c9c3295e-716f-4093-b437-f6c405f5bc7b
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMMultiMediaStream interface [DirectShow],Initialize method, IAMMultiMediaStream.Initialize, IAMMultiMediaStream::Initialize, IAMMultiMediaStreamInitialize, Initialize, Initialize method [DirectShow], Initialize method [DirectShow],IAMMultiMediaStream interface, amstream/IAMMultiMediaStream::Initialize, dshow.iammultimediastream_initialize
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
 - IAMMultiMediaStream.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMultiMediaStream::Initialize


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>Initialize</code> method initializes the multimedia stream object.




## -parameters




### -param StreamType [in]

Member of the <a href="https://msdn.microsoft.com/07ab5ded-28b8-4cac-b4da-76f07ad351ef">STREAM_TYPE</a> enumeration, specifying whether the streams are read-only, write-only, or read/write.


### -param dwFlags [in]

Must be one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Zero</td>
<td>Create a filter graph that runs on a separate thread.</td>
</tr>
<tr>
<td>AMMSF_NOGRAPHTHREAD</td>
<td>Create a filter graph that runs on the calling thread.</td>
</tr>
</table>
 


### -param pFilterGraph [in]

[optional] Pointer to the <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface, or <b>NULL</b>. If this parameter is non-<b>NULL</b>, it specifies a filter graph that the multimedia stream object will use. Otherwise, the multimedia stream object creates a new filter graph.


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
 




## -remarks



If you specify AMMSF_NOGRAPHTHREAD in the <i>dwFlags</i> parameter, the calling thread must process window messages, and it must release all multimedia streaming objects before the thread exits. Otherwise, the application might deadlock.




## -see-also




<a href="https://msdn.microsoft.com/2f604156-68ef-4770-9929-6dbfd46c4d6d">IAMMultiMediaStream Interface</a>
 

 

