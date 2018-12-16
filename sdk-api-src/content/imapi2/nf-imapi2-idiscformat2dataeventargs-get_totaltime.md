---
UID: NF:imapi2.IDiscFormat2DataEventArgs.get_TotalTime
title: IDiscFormat2DataEventArgs::get_TotalTime
author: windows-sdk-content
description: Retrieves the estimated total time for write operation.
old-location: imapi\idiscformat2dataeventargs_get_totaltime.htm
tech.root: imapi
ms.assetid: 95e61ef9-5d1c-4f29-896f-69a56c23f306
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiscFormat2DataEventArgs interface [IMAPI],get_TotalTime method, IDiscFormat2DataEventArgs.get_TotalTime, IDiscFormat2DataEventArgs::get_TotalTime, get_TotalTime, get_TotalTime method [IMAPI], get_TotalTime method [IMAPI],IDiscFormat2DataEventArgs interface, imapi.idiscformat2dataeventargs_get_totaltime, imapi2/IDiscFormat2DataEventArgs::get_TotalTime
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
 - IDiscFormat2DataEventArgs.get_TotalTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2DataEventArgs::get_TotalTime


## -description


Retrieves the estimated total time for write operation.


## -parameters




### -param value [out]

Estimated time, in seconds, for write operation. 


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



The estimate for a single write operation can vary as the operation progresses. The drive provides updated information that can affect the projected duration of the write operation.




## -see-also




<a href="https://msdn.microsoft.com/f9f1d976-9ec9-40a5-92b6-d00a7e15d0aa">DDiscFormat2DataEvents</a>



<a href="https://msdn.microsoft.com/6bf149d3-62ea-4ef5-8d45-44df9ad4982c">IDiscFormat2DataEventArgs</a>
 

 

