---
UID: NF:imapi2.IDiscFormat2RawCD.get_RequestedSectorType
title: IDiscFormat2RawCD::get_RequestedSectorType
author: windows-driver-content
description: Retrieves the requested data sector to use during write of the stream.
old-location: imapi\idiscformat2rawcd__get_requestedsectortype_.htm
old-project: imapi
ms.assetid: 7964e25e-43ed-4ed0-aeee-dac656700fea
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],get_RequestedSectorType method, IDiscFormat2RawCD.get_RequestedSectorType, IDiscFormat2RawCD::get_RequestedSectorType, get_RequestedSectorType, get_RequestedSectorType method [IMAPI], get_RequestedSectorType method [IMAPI],IDiscFormat2RawCD interface, imapi.idiscformat2rawcd__get_requestedsectortype_, imapi2/IDiscFormat2RawCD::get_RequestedSectorType
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
-	IDiscFormat2RawCD.get_RequestedSectorType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2RawCD::get_RequestedSectorType


## -description


Retrieves the requested data sector to use during write of the stream.


## -parameters




### -param value [out]

Requested data sector type. For possible values, see <a href="https://msdn.microsoft.com/f3193377-5410-4cd2-b7e5-281b3794c583">IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE</a>. 


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
<dt><b>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
The requested operation is only valid when media has been "prepared".

Value: 0xC0AA0602

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>



<a href="https://msdn.microsoft.com/d217e585-3ff4-4f02-8a13-7cfca767f201">IDiscFormat2RawCD::get_SupportedSectorTypes</a>



<a href="https://msdn.microsoft.com/fd9d7e1d-5672-482f-ac83-efcab3adbac4">IDiscFormat2RawCD::put_RequestedSectorType</a>
 

 

