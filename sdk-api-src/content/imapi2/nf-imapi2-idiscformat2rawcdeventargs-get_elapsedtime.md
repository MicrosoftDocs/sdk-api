---
UID: NF:imapi2.IDiscFormat2RawCDEventArgs.get_ElapsedTime
title: IDiscFormat2RawCDEventArgs::get_ElapsedTime
author: windows-sdk-content
description: Retrieves the total elapsed time of the write operation.
old-location: imapi\idiscformat2rawcdeventargs_get_elapsedtime.htm
tech.root: imapi
ms.assetid: 87a1b606-f91b-4a14-b3b0-17d224d841fc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiscFormat2RawCDEventArgs interface [IMAPI],get_ElapsedTime method, IDiscFormat2RawCDEventArgs.get_ElapsedTime, IDiscFormat2RawCDEventArgs::get_ElapsedTime, get_ElapsedTime, get_ElapsedTime method [IMAPI], get_ElapsedTime method [IMAPI],IDiscFormat2RawCDEventArgs interface, imapi.idiscformat2rawcdeventargs_get_elapsedtime, imapi2/IDiscFormat2RawCDEventArgs::get_ElapsedTime
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
 - IDiscFormat2RawCDEventArgs.get_ElapsedTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2RawCDEventArgs::get_ElapsedTime


## -description


Retrieves the total elapsed time of the write operation.


## -parameters




### -param value [out]

Elapsed time, in seconds, of the write operation. 


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




<a href="https://msdn.microsoft.com/3a06911e-8a50-4e41-874c-478ad05f6488">DDiscFormat2RawCDEvents</a>



<a href="https://msdn.microsoft.com/b1988883-459c-46f1-a0d1-df9500a000e1">IDiscFormat2RawCDEventArgs</a>
 

 

