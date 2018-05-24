---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.get_ClientName
title: IDiscFormat2TrackAtOnce::get_ClientName
author: windows-driver-content
description: Retrieves the friendly name of the client.
old-location: imapi\idiscformat2trackatonce_get_clientname.htm
old-project: imapi
ms.assetid: c259233b-4e36-4ee2-8068-d77ece1e927e
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: IDiscFormat2TrackAtOnce interface [IMAPI],get_ClientName method, IDiscFormat2TrackAtOnce.get_ClientName, IDiscFormat2TrackAtOnce::get_ClientName, get_ClientName, get_ClientName method [IMAPI], get_ClientName method [IMAPI],IDiscFormat2TrackAtOnce interface, imapi.idiscformat2trackatonce_get_clientname, imapi2/IDiscFormat2TrackAtOnce::get_ClientName
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
-	IDiscFormat2TrackAtOnce.get_ClientName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2TrackAtOnce::get_ClientName


## -description


Retrieves the friendly name of the client.


## -parameters




### -param value [out]

Name supplied by the client application.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/27f2d248-1c83-4784-82f9-75ce0a038b87">IDiscFormat2TrackAtOnce</a>



<a href="https://msdn.microsoft.com/9140aa9f-f592-4ef4-85c7-321e5503b0b8">IDiscFormat2TrackAtOnce::put_ClientName</a>
 

 

