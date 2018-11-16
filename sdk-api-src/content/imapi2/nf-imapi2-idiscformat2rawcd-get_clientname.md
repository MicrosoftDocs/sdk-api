---
UID: NF:imapi2.IDiscFormat2RawCD.get_ClientName
title: IDiscFormat2RawCD::get_ClientName
author: windows-sdk-content
description: Retrieves the friendly name of the client.
old-location: imapi\idiscformat2rawcd_get_clientname.htm
tech.root: imapi
ms.assetid: dd706b68-0dde-4a44-b5f5-764fad56844f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],get_ClientName method, IDiscFormat2RawCD.get_ClientName, IDiscFormat2RawCD::get_ClientName, get_ClientName, get_ClientName method [IMAPI], get_ClientName method [IMAPI],IDiscFormat2RawCD interface, imapi.idiscformat2rawcd_get_clientname, imapi2/IDiscFormat2RawCD::get_ClientName
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
 - IDiscFormat2RawCD.get_ClientName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imapi2.h
: 
- IDiscFormat2RawCD.get_ClientName
: 
---

# IDiscFormat2RawCD::get_ClientName


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




<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>



<a href="https://msdn.microsoft.com/9140aa9f-f592-4ef4-85c7-321e5503b0b8">IDiscFormat2TrackAtOnce::put_ClientName</a>
 

 

