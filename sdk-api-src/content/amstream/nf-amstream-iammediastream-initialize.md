---
UID: NF:amstream.IAMMediaStream.Initialize
title: IAMMediaStream::Initialize
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The Initialize method creates and initializes a new media stream with the specified stream type and purpose ID.
old-location: dshow\iammediastream_initialize.htm
tech.root: DirectShow
ms.assetid: b695100b-75a4-4107-828c-e0067290d972
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMMediaStream interface [DirectShow],Initialize method, IAMMediaStream.Initialize, IAMMediaStream::Initialize, IAMMediaStreamInitialize, Initialize, Initialize method [DirectShow], Initialize method [DirectShow],IAMMediaStream interface, amstream/IAMMediaStream::Initialize, dshow.iammediastream_initialize
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
 - IAMMediaStream.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaStream::Initialize


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>Initialize</code> method creates and initializes a new media stream with the specified stream type and purpose ID.




## -parameters




### -param pSourceObject [in]

Pointer to an <b>IUnknown</b> source object.


### -param dwFlags [in]

Value that modifies the media stream's behavior; it is a combination of one or more of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description</th>
</tr>
<tr>
<td>AMMSF_ADDDEFAULTRENDERER</td>
<td>Add a default renderer.</td>
</tr>
<tr>
<td>AMMSF_CREATEPEER</td>
<td>Create a peer stream based on the same object as a <i>pStreamObject</i>.</td>
</tr>
<tr>
<td>AMMSF_NOSTALL</td>
<td>Run the stream even if <a href="https://msdn.microsoft.com/5f56e3f9-443b-4d67-bfed-3210e691ad4b">Update</a> is not called.</td>
</tr>
<tr>
<td>AMMSF_STOPIFNOSAMPLES</td>
<td>Terminates the stream if no samples were created or if the last sample is deleted.</td>
</tr>
</table>
 


### -param PurposeId

TBD


### -param StreamType [in]


<a href="https://msdn.microsoft.com/07ab5ded-28b8-4cac-b4da-76f07ad351ef">STREAM_TYPE</a> enumeration value that specifies the new media stream's media type.


#### - PurposeID [in]

Purpose ID for the new media stream.


## -returns



Returns S_OK if successful or E_POINTER if one or more of the required parameters are invalid.




## -remarks



If <i>dwFlags</i> specifies AMMSF_ADDDEFAULTRENDERER, then the default renderer for the given purpose ID is created, if possible. Currently, the only default renderer supported is for audio using DirectSound. In this case, the <i>pStreamObject</i> parameter must be <b>NULL</b> and any calls to the <a href="https://msdn.microsoft.com/d85cde4f-99f4-4641-b75f-13ca6dc7f21e">IMultiMediaStream::GetMediaStream</a> or <a href="https://msdn.microsoft.com/2fb51794-83ac-44c5-b388-d7b945870324">IMultiMediaStream::EnumMediaStreams</a> method will not recognize the stream.

If <i>dwFlags</i> specifies AMMSF_CREATEPEER, then a media stream is created using <i>pStreamObject</i> and added to the current multimedia stream. The <i>pStreamObject</i> parameter varies depending on the stream type. In general, <i>pStreamObject</i> can point to an <a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream</a> object, in which case a stream with the sample purpose ID and format is created. For <b>IDirectDraw</b> streams, it can also be a pointer to an <b>IDirectDraw</b> interface.

If <i>dwFlags</i> specifies AMMSF_STOPIFNOSAMPLES, then the stream is terminated.

If no flags are set, then <i>pStreamObject</i> can be one of the following.

<table>
<tr>
<th>Value
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>An <a href="https://msdn.microsoft.com/14185e7d-d08d-4fd8-a255-075eaf12a708">IAMMediaStream</a> object</td>
<td>This stream is then added to the streams in the multimedia stream.</td>
</tr>
<tr>
<td><b>NULL</b></td>
<td>In this case a default <a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream</a> object is added to the stream with a default underlying object, if required.</td>
</tr>
<tr>
<td>A pointer to an underlying object</td>
<td>This is used to construct default streams. For video streams, this can be an <b>IDirectDraw</b> pointer.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/14185e7d-d08d-4fd8-a255-075eaf12a708">IAMMediaStream Interface</a>
 

 

