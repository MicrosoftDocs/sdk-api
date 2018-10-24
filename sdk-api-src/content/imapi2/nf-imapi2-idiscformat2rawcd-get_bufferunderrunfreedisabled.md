---
UID: NF:imapi2.IDiscFormat2RawCD.get_BufferUnderrunFreeDisabled
title: IDiscFormat2RawCD::get_BufferUnderrunFreeDisabled
author: windows-sdk-content
description: Determines if Buffer Underrun Free recording is enabled.
old-location: imapi\idiscformat2rawcd_get_bufferunderrunfreedisabled.htm
tech.root: imapi
ms.assetid: 85b20760-334e-47a1-9683-be3d76c8958f
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],get_BufferUnderrunFreeDisabled method, IDiscFormat2RawCD.get_BufferUnderrunFreeDisabled, IDiscFormat2RawCD::get_BufferUnderrunFreeDisabled, get_BufferUnderrunFreeDisabled, get_BufferUnderrunFreeDisabled method [IMAPI], get_BufferUnderrunFreeDisabled method [IMAPI],IDiscFormat2RawCD interface, imapi.idiscformat2rawcd_get_bufferunderrunfreedisabled, imapi2/IDiscFormat2RawCD::get_BufferUnderrunFreeDisabled
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
 - IDiscFormat2RawCD.get_BufferUnderrunFreeDisabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2RawCD::get_BufferUnderrunFreeDisabled


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




<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>



<a href="https://msdn.microsoft.com/66b35ca9-2bc7-419e-8fff-4449a64f9f5f">IDiscFormat2RawCD::put_BufferUnderrunFreeDisabled</a>
 

 

