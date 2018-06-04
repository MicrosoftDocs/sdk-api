---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDiscFormat2RawCD::put_RequestedSectorType


## -description


Sets the requested data sector to use for writing the stream.


## -parameters




### -param value [in]

Data sector to use for writing the stream. For possible values, see the <a href="https://msdn.microsoft.com/f3193377-5410-4cd2-b7e5-281b3794c583">IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE</a> enumeration type. The default is <b>IMAPI_FORMAT2_RAW_CD_SUBCODE_IS_COOKED</b>.


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
<dt><b>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
There is currently a write operation in progress.

Value: 0xC0AA0600

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
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The requested data block type is not supported by the current device.

Value: 0xC0AA060E

</td>
</tr>
</table>
 




## -remarks



For a list of supported data sector types, call the <a href="https://msdn.microsoft.com/d217e585-3ff4-4f02-8a13-7cfca767f201">IDiscFormat2RawCD::get_SupportedSectorTypes</a> method.




## -see-also




<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>



<a href="https://msdn.microsoft.com/7964e25e-43ed-4ed0-aeee-dac656700fea">IDiscFormat2RawCD::get_RequestedSectorType</a>



<a href="https://msdn.microsoft.com/d217e585-3ff4-4f02-8a13-7cfca767f201">IDiscFormat2RawCD::get_SupportedSectorTypes</a>
 

 

