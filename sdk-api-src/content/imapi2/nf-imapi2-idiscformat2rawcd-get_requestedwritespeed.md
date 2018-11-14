---
UID: NF:imapi2.IDiscFormat2RawCD.get_RequestedWriteSpeed
title: IDiscFormat2RawCD::get_RequestedWriteSpeed
author: windows-sdk-content
description: Retrieves the requested write speed.
old-location: imapi\idiscformat2rawcd_get_requestedwritespeed.htm
tech.root: imapi
ms.assetid: 0b718fe5-197e-4dc7-a8df-f2febf76aaab
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],get_RequestedWriteSpeed method, IDiscFormat2RawCD.get_RequestedWriteSpeed, IDiscFormat2RawCD::get_RequestedWriteSpeed, get_RequestedWriteSpeed, get_RequestedWriteSpeed method [IMAPI], get_RequestedWriteSpeed method [IMAPI],IDiscFormat2RawCD interface, imapi.idiscformat2rawcd_get_requestedwritespeed, imapi2/IDiscFormat2RawCD::get_RequestedWriteSpeed
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
 - IDiscFormat2RawCD.get_RequestedWriteSpeed
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
- IDiscFormat2RawCD.get_RequestedWriteSpeed
: 
---

# IDiscFormat2RawCD::get_RequestedWriteSpeed


## -description


Retrieves the requested write speed.


## -parameters




### -param value [out]

Requested write speed measured in disc sectors per second.

A value of 0xFFFFFFFF (-1) requests that the write occurs using the fastest supported speed for the media.  


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
 




## -remarks



This is the value specified in the most recent call to the <a href="https://msdn.microsoft.com/93021007-6ed8-4322-93bb-c52796a4ab66">IDiscFormat2RawCD::SetWriteSpeed</a> method.




## -see-also




<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>



<a href="https://msdn.microsoft.com/93021007-6ed8-4322-93bb-c52796a4ab66">IDiscFormat2RawCD::SetWriteSpeed</a>



<a href="https://msdn.microsoft.com/f369f719-7db6-4a79-a5fa-d174bf12acbc">IDiscFormat2RawCD::get_CurrentWriteSpeed</a>



<a href="https://msdn.microsoft.com/7ebcc42f-d864-407f-a1a6-d4811ca8221c">IDiscFormat2RawCD::get_SupportedWriteSpeeds</a>
 

 

