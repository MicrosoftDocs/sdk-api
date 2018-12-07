---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.get_DoNotFinalizeMedia
title: IDiscFormat2TrackAtOnce::get_DoNotFinalizeMedia
author: windows-sdk-content
description: Determines if the media is left open for writing after writing the audio track.
old-location: imapi\idiscformat2trackatonce_get_donotfinalizemedia.htm
tech.root: imapi
ms.assetid: 7f33bbc2-531a-472a-8e2a-b7e9fb4d6bba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiscFormat2TrackAtOnce interface [IMAPI],get_DoNotFinalizeMedia method, IDiscFormat2TrackAtOnce.get_DoNotFinalizeMedia, IDiscFormat2TrackAtOnce::get_DoNotFinalizeMedia, get_DoNotFinalizeMedia, get_DoNotFinalizeMedia method [IMAPI], get_DoNotFinalizeMedia method [IMAPI],IDiscFormat2TrackAtOnce interface, imapi.idiscformat2trackatonce_get_donotfinalizemedia, imapi2/IDiscFormat2TrackAtOnce::get_DoNotFinalizeMedia
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
 - IDiscFormat2TrackAtOnce.get_DoNotFinalizeMedia
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2TrackAtOnce::get_DoNotFinalizeMedia


## -description


Determines if the media is left open for writing after writing the audio track.


## -parameters




### -param value [out]

Is VARIANT_TRUE if the media is left open for writing after writing the audio track; otherwise, VARIANT_FALSE.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/27f2d248-1c83-4784-82f9-75ce0a038b87">IDiscFormat2TrackAtOnce</a>



<a href="https://msdn.microsoft.com/29a0a857-c515-4265-b0b6-6e2048f3de18">IDiscFormat2TrackAtOnce::PrepareMedia</a>



<a href="https://msdn.microsoft.com/0d6f85a9-94cc-426c-8442-14eb6e4024f3">IDiscFormat2TrackAtOnce::ReleaseMedia</a>



<a href="https://msdn.microsoft.com/ffde10f9-259a-400d-b83e-f8c81bbe8f94">IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia</a>
 

 

