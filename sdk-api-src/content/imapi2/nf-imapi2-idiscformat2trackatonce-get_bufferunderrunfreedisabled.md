---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.get_BufferUnderrunFreeDisabled
title: IDiscFormat2TrackAtOnce::get_BufferUnderrunFreeDisabled method
author: windows-driver-content
description: Determines if Buffer Underrun Free recording is enabled.
old-location: imapi\idiscformat2trackatonce_get_bufferunderrunfreedisabled.htm
old-project: imapi
ms.assetid: 8223c46b-b754-47a1-aab9-0ebb949e79f8
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IDiscFormat2TrackAtOnce, IDiscFormat2TrackAtOnce interface [IMAPI], get_BufferUnderrunFreeDisabled method, IDiscFormat2TrackAtOnce::get_BufferUnderrunFreeDisabled, get_BufferUnderrunFreeDisabled method [IMAPI], get_BufferUnderrunFreeDisabled method [IMAPI], IDiscFormat2TrackAtOnce interface, get_BufferUnderrunFreeDisabled,IDiscFormat2TrackAtOnce.get_BufferUnderrunFreeDisabled, imapi.idiscformat2trackatonce_get_bufferunderrunfreedisabled, imapi2/IDiscFormat2TrackAtOnce::get_BufferUnderrunFreeDisabled
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
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IDiscFormat2TrackAtOnce.get_BufferUnderrunFreeDisabled
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2TrackAtOnce::get_BufferUnderrunFreeDisabled method


## -description


Determines if Buffer Underrun Free recording is enabled.


## -parameters




### -param value [out]

Is VARIANT_TRUE if Buffer Underrun Free recording is disabled; otherwise, VARIANT_FALSE (enabled).


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



<a href="https://msdn.microsoft.com/93a19bd7-9302-49f5-a5e5-573bf72725a3">IDiscFormat2TrackAtOnce::put_BufferUnderrunFreeDisabled</a>
 

 

