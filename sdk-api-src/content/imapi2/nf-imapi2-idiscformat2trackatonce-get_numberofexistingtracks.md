---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.get_NumberOfExistingTracks
title: IDiscFormat2TrackAtOnce::get_NumberOfExistingTracks
author: windows-sdk-content
description: Retrieves the number of existing audio tracks on the media.
old-location: imapi\idiscformat2trackatonce_get_numberofexistingtracks.htm
tech.root: imapi
ms.assetid: 6a8bcfe2-d09a-4eec-8e68-5e0dfc868033
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDiscFormat2TrackAtOnce interface [IMAPI],get_NumberOfExistingTracks method, IDiscFormat2TrackAtOnce.get_NumberOfExistingTracks, IDiscFormat2TrackAtOnce::get_NumberOfExistingTracks, get_NumberOfExistingTracks, get_NumberOfExistingTracks method [IMAPI], get_NumberOfExistingTracks method [IMAPI],IDiscFormat2TrackAtOnce interface, imapi.idiscformat2trackatonce_get_numberofexistingtracks, imapi2/IDiscFormat2TrackAtOnce::get_NumberOfExistingTracks
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IDiscFormat2TrackAtOnce.get_NumberOfExistingTracks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2TrackAtOnce::get_NumberOfExistingTracks


## -description


Retrieves the number of existing audio tracks on the media.


## -parameters




### -param value [out]

Number of completed tracks written to disc, not including the track currently being added.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

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
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
The media is not prepared (IDiscFormat2TrackAtOnce::PrepareMedia has not been called).

Value: 0xC0AA0502

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
A write operation is in progress.

Value: 0xC0AA0500

</td>
</tr>
</table>
 




## -remarks



The value is zero if:

<ul>
<li>The media is blank</li>
<li>You call this method outside a writing session</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/27f2d248-1c83-4784-82f9-75ce0a038b87">IDiscFormat2TrackAtOnce</a>



<a href="https://msdn.microsoft.com/3ac74b91-b0c7-471f-b6a9-1393d677e0c1">IDiscFormat2TrackAtOnce::AddAudioTrack</a>



<a href="https://msdn.microsoft.com/29a0a857-c515-4265-b0b6-6e2048f3de18">IDiscFormat2TrackAtOnce::PrepareMedia</a>



<a href="https://msdn.microsoft.com/0d6f85a9-94cc-426c-8442-14eb6e4024f3">IDiscFormat2TrackAtOnce::ReleaseMedia</a>
 

 

