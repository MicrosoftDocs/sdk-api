---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.put_DoNotFinalizeMedia
title: IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia
author: windows-sdk-content
description: Determines if the media is left open for writing after writing the audio track.
old-location: imapi\idiscformat2trackatonce_put_donotfinalizemedia.htm
tech.root: imapi
ms.assetid: ffde10f9-259a-400d-b83e-f8c81bbe8f94
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IDiscFormat2TrackAtOnce interface [IMAPI],put_DoNotFinalizeMedia method, IDiscFormat2TrackAtOnce.put_DoNotFinalizeMedia, IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia, imapi.idiscformat2trackatonce_put_donotfinalizemedia, imapi2/IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia, put_DoNotFinalizeMedia, put_DoNotFinalizeMedia method [IMAPI], put_DoNotFinalizeMedia method [IMAPI],IDiscFormat2TrackAtOnce interface
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
 - IDiscFormat2TrackAtOnce.put_DoNotFinalizeMedia
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia


## -description


Determines if the media is left open for writing after writing the audio track.


## -parameters




### -param value [in]

Set to VARIANT_TRUE to leave the media open for writing after writing the audio track; otherwise, VARIANT_FALSE. The default is VARIANT_FALSE.


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
<dt><b>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
A write operation is in progress.

Value: 0xC0AA0500

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
The requested operation is not valid when media has been "prepared" but not released.

Value: 0xC0AA0503

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The property cannot be changed once the media has been written to.

Value: 0xC0AA0504

</td>
</tr>
</table>
 




## -remarks



You can set this property before calling the <a href="https://msdn.microsoft.com/29a0a857-c515-4265-b0b6-6e2048f3de18">IDiscFormat2TrackAtOnce::PrepareMedia</a> method or after calling the <a href="https://msdn.microsoft.com/0d6f85a9-94cc-426c-8442-14eb6e4024f3">IDiscFormat2TrackAtOnce::ReleaseMedia</a> method; you cannot set it during a track-writing session. 

This property is useful to create a multi-session CD with audio in the first session and data in the second session.




## -see-also




<a href="https://msdn.microsoft.com/27f2d248-1c83-4784-82f9-75ce0a038b87">IDiscFormat2TrackAtOnce</a>



<a href="https://msdn.microsoft.com/29a0a857-c515-4265-b0b6-6e2048f3de18">IDiscFormat2TrackAtOnce::PrepareMedia</a>



<a href="https://msdn.microsoft.com/0d6f85a9-94cc-426c-8442-14eb6e4024f3">IDiscFormat2TrackAtOnce::ReleaseMedia</a>



<a href="https://msdn.microsoft.com/7f33bbc2-531a-472a-8e2a-b7e9fb4d6bba">IDiscFormat2TrackAtOnce::get_DoNotFinalizeMedia</a>
 

 

