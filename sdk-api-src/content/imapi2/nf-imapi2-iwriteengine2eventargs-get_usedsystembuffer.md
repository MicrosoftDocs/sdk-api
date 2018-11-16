---
UID: NF:imapi2.IWriteEngine2EventArgs.get_UsedSystemBuffer
title: IWriteEngine2EventArgs::get_UsedSystemBuffer
author: windows-sdk-content
description: Retrieves the number of used bytes in the internal data buffer that is used for writing to disc.
old-location: imapi\iwriteengine2eventargs_get_usedsystembuffer.htm
tech.root: imapi
ms.assetid: 905c476f-33cd-4eda-a342-c7a20479d63c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWriteEngine2EventArgs interface [IMAPI],get_UsedSystemBuffer method, IWriteEngine2EventArgs.get_UsedSystemBuffer, IWriteEngine2EventArgs::get_UsedSystemBuffer, get_UsedSystemBuffer, get_UsedSystemBuffer method [IMAPI], get_UsedSystemBuffer method [IMAPI],IWriteEngine2EventArgs interface, imapi.iwriteengine2eventargs_get_usedsystembuffer, imapi2/IWriteEngine2EventArgs::get_UsedSystemBuffer
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
 - IWriteEngine2EventArgs.get_UsedSystemBuffer
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
- IWriteEngine2EventArgs.get_UsedSystemBuffer
: 
---

# IWriteEngine2EventArgs::get_UsedSystemBuffer


## -description


Retrieves the number of used bytes in the internal data buffer that is used for writing to disc.


## -parameters




### -param value [out]

Size, in bytes, of the used portion  of the internal data buffer that is used for writing to disc.


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



This value increases as data is read into the buffer and decreases as data is written to disc.




## -see-also




<a href="https://msdn.microsoft.com/1922410a-5871-477f-b778-36b12ad95168">IWriteEngine2EventArgs</a>



<a href="https://msdn.microsoft.com/d62eeb31-cf47-4456-832c-9a29c045b11c">IWriteEngine2EventArgs::get_FreeSystemBuffer</a>



<a href="https://msdn.microsoft.com/dfdf4116-0402-4c90-8b9b-0758fd0bb973">IWriteEngine2EventArgs::get_TotalSystemBuffer</a>
 

 

