---
UID: NF:imapi2.IDiscMaster2.get_Count
title: IDiscMaster2::get_Count
author: windows-sdk-content
description: Retrieves the number of the CD and DVD disc devices installed on the computer.
old-location: imapi\idiscmaster2_get_count.htm
old-project: imapi
ms.assetid: b1e0ec8f-4c66-4648-ad76-2998200ea574
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IDiscMaster2 interface [IMAPI],get_Count method, IDiscMaster2.get_Count, IDiscMaster2::get_Count, get_Count, get_Count method [IMAPI], get_Count method [IMAPI],IDiscMaster2 interface, imapi.idiscmaster2_get_count, imapi2/IDiscMaster2::get_Count
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
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IDiscMaster2.get_Count
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscMaster2::get_Count


## -description


Retrieves the number of the CD and DVD disc devices installed on the computer.


## -parameters




### -param value [out]

Number of CD and DVD disc devices installed on the computer.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified failure.

Value: 0x80004005

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cdca44d4-6ab5-4c2f-91ba-bef79b1d457e">IDiscMaster2</a>



<a href="https://msdn.microsoft.com/e909acb9-850b-404d-a2f7-efb37faf3506">IDiscMaster2::get_Item</a>



<a href="https://msdn.microsoft.com/f148a1c0-cb76-40e9-9749-a074f04c93e8">IDiscMaster::__NewEnum</a>
 

 

