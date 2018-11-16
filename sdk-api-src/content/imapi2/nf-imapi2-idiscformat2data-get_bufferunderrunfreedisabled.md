---
UID: NF:imapi2.IDiscFormat2Data.get_BufferUnderrunFreeDisabled
title: IDiscFormat2Data::get_BufferUnderrunFreeDisabled
author: windows-sdk-content
description: Determines if Buffer Underrun Free recording is enabled for CDR, CD-RW, and DVD-R media.
old-location: imapi\idiscformat2data_get_bufferunderrunfreedisabled.htm
tech.root: imapi
ms.assetid: 2b85f13c-33c2-4b19-9b70-5a829f9de3ea
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],get_BufferUnderrunFreeDisabled method, IDiscFormat2Data.get_BufferUnderrunFreeDisabled, IDiscFormat2Data::get_BufferUnderrunFreeDisabled, get_BufferUnderrunFreeDisabled, get_BufferUnderrunFreeDisabled method [IMAPI], get_BufferUnderrunFreeDisabled method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_get_bufferunderrunfreedisabled, imapi2/IDiscFormat2Data::get_BufferUnderrunFreeDisabled
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
 - IDiscFormat2Data.get_BufferUnderrunFreeDisabled
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
- IDiscFormat2Data.get_BufferUnderrunFreeDisabled
: 
---

# IDiscFormat2Data::get_BufferUnderrunFreeDisabled


## -description


Determines if Buffer Underrun Free recording is enabled for CDR, CD-RW, and DVD-R media.


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




<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/32d05abe-c434-4a87-b6ee-961a999321c5">IDiscFormat2Data::put_BufferUnderrunFreeDisabled</a>
 

 

