---
UID: NF:imapi2.IDiscRecorder2.get_VendorId
title: IDiscRecorder2::get_VendorId
author: windows-driver-content
description: Retrieves the vendor ID for the device.
old-location: imapi\idiscrecorder2_get_vendorid.htm
old-project: imapi
ms.assetid: a3e76907-1960-4c13-b6e4-9f5c86de38c6
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IDiscRecorder2 interface [IMAPI],get_VendorId method, IDiscRecorder2.get_VendorId, IDiscRecorder2::get_VendorId, get_VendorId, get_VendorId method [IMAPI], get_VendorId method [IMAPI],IDiscRecorder2 interface, imapi.idiscrecorder2_get_vendorid, imapi2/IDiscRecorder2::get_VendorId
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
-	IDiscRecorder2.get_VendorId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscRecorder2::get_VendorId


## -description


Retrieves the vendor ID for the device.


## -parameters




### -param value [out]

String that contains the vendor ID for the device.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified failure.

Value: 0x80004005

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




<a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a>
 

 

