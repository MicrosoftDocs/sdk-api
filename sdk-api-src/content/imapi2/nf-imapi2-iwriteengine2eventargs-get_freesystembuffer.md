---
UID: NF:imapi2.IWriteEngine2EventArgs.get_FreeSystemBuffer
title: IWriteEngine2EventArgs::get_FreeSystemBuffer method
author: windows-driver-content
description: Retrieves the number of unused bytes in the internal data buffer that is used for writing to disc.
old-location: imapi\iwriteengine2eventargs_get_freesystembuffer.htm
old-project: imapi
ms.assetid: d62eeb31-cf47-4456-832c-9a29c045b11c
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IWriteEngine2EventArgs, IWriteEngine2EventArgs interface [IMAPI], get_FreeSystemBuffer method, IWriteEngine2EventArgs::get_FreeSystemBuffer, get_FreeSystemBuffer method [IMAPI], get_FreeSystemBuffer method [IMAPI], IWriteEngine2EventArgs interface, get_FreeSystemBuffer,IWriteEngine2EventArgs.get_FreeSystemBuffer, imapi.iwriteengine2eventargs_get_freesystembuffer, imapi2/IWriteEngine2EventArgs::get_FreeSystemBuffer
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
-	IWriteEngine2EventArgs.get_FreeSystemBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWriteEngine2EventArgs::get_FreeSystemBuffer method


## -description


Retrieves the number of unused bytes in the internal data buffer that is used for writing to disc.


## -parameters




### -param value [out]

Size, in bytes, of the unused portion  of the internal data buffer that is used for writing to disc.


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



This method returns the same value as if you subtracted <a href="https://msdn.microsoft.com/905c476f-33cd-4eda-a342-c7a20479d63c">IWriteEngine2EventArgs::get_UsedSystemBuffer</a> from <a href="https://msdn.microsoft.com/dfdf4116-0402-4c90-8b9b-0758fd0bb973">IWriteEngine2EventArgs::get_TotalSystemBuffer</a>.




## -see-also




<a href="https://msdn.microsoft.com/1922410a-5871-477f-b778-36b12ad95168">IWriteEngine2EventArgs</a>



<a href="https://msdn.microsoft.com/dfdf4116-0402-4c90-8b9b-0758fd0bb973">IWriteEngine2EventArgs::get_TotalSystemBuffer</a>



<a href="https://msdn.microsoft.com/905c476f-33cd-4eda-a342-c7a20479d63c">IWriteEngine2EventArgs::get_UsedSystemBuffer</a>
 

 

