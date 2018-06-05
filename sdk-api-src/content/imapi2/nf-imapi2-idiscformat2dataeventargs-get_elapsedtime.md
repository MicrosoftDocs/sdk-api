---
UID: NF:imapi2.IDiscFormat2DataEventArgs.get_ElapsedTime
title: IDiscFormat2DataEventArgs::get_ElapsedTime
author: windows-sdk-content
description: Retrieves the total elapsed time of the write operation.
old-location: imapi\idiscformat2dataeventargs_get_elapsedtime.htm
old-project: imapi
ms.assetid: 5ac3c261-dedc-4316-9241-387fc222443d
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IDiscFormat2DataEventArgs interface [IMAPI],get_ElapsedTime method, IDiscFormat2DataEventArgs.get_ElapsedTime, IDiscFormat2DataEventArgs::get_ElapsedTime, get_ElapsedTime, get_ElapsedTime method [IMAPI], get_ElapsedTime method [IMAPI],IDiscFormat2DataEventArgs interface, imapi.idiscformat2dataeventargs_get_elapsedtime, imapi2/IDiscFormat2DataEventArgs::get_ElapsedTime
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IDiscFormat2DataEventArgs.get_ElapsedTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2DataEventArgs::get_ElapsedTime


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




<a href="https://msdn.microsoft.com/f9f1d976-9ec9-40a5-92b6-d00a7e15d0aa">DDiscFormat2DataEvents</a>



<a href="https://msdn.microsoft.com/6bf149d3-62ea-4ef5-8d45-44df9ad4982c">IDiscFormat2DataEventArgs</a>
 

 

