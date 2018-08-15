---
UID: NF:imapi2.IDiscRecorder2.get_ProductRevision
title: IDiscRecorder2::get_ProductRevision
author: windows-sdk-content
description: Retrieves the product revision code of the device.
old-location: imapi\idiscrecorder2_get_productrevision.htm
old-project: imapi
ms.assetid: 0d727937-8581-4001-96f2-f83795e1ee52
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IDiscRecorder2 interface [IMAPI],get_ProductRevision method, IDiscRecorder2.get_ProductRevision, IDiscRecorder2::get_ProductRevision, get_ProductRevision, get_ProductRevision method [IMAPI], get_ProductRevision method [IMAPI],IDiscRecorder2 interface, imapi.idiscrecorder2_get_productrevision, imapi2/IDiscRecorder2::get_ProductRevision
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscRecorder2.get_ProductRevision
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscRecorder2::get_ProductRevision


## -description


Retrieves the product revision code of the device.


## -parameters




### -param value [out]

String that contains the product revision code of the device.


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
 

 

