---
UID: NF:imapi2.IDiscFormat2RawCD.put_BufferUnderrunFreeDisabled
title: IDiscFormat2RawCD::put_BufferUnderrunFreeDisabled
author: windows-sdk-content
description: Determines if Buffer Underrun Free recording is enabled.
old-location: imapi\idiscformat2rawcd_put_bufferunderrunfreedisabled.htm
tech.root: imapi
ms.assetid: 66b35ca9-2bc7-419e-8fff-4449a64f9f5f
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],put_BufferUnderrunFreeDisabled method, IDiscFormat2RawCD.put_BufferUnderrunFreeDisabled, IDiscFormat2RawCD::put_BufferUnderrunFreeDisabled, imapi.idiscformat2rawcd_put_bufferunderrunfreedisabled, imapi2/IDiscFormat2RawCD::put_BufferUnderrunFreeDisabled, put_BufferUnderrunFreeDisabled, put_BufferUnderrunFreeDisabled method [IMAPI], put_BufferUnderrunFreeDisabled method [IMAPI],IDiscFormat2RawCD interface
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
 - IDiscFormat2RawCD.put_BufferUnderrunFreeDisabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2RawCD::put_BufferUnderrunFreeDisabled


## -description


Determines if Buffer Underrun Free recording is enabled. 


## -parameters




### -param value [in]

Set to VARIANT_TRUE to disable Buffer Underrun Free recording; otherwise, VARIANT_FALSE. The default is VARIANT_FALSE (enabled).


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
<dt><b>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
There is currently a write operation in progress.

Value: 0xC0AA0600

</td>
</tr>
</table>
 




## -remarks



Buffer underrun can be an issue if the data stream does not enter the buffer fast enough to keep the device continuously writing. In turn, the stop and start action of writing can cause data on the disc to be unusable. Buffer Underrun Free (BUF) recording allows the laser to start and stop without damaging data already written to the disc. Disabling of BUF recording is possible only on CD-R/RW media.




## -see-also




<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>



<a href="https://msdn.microsoft.com/85b20760-334e-47a1-9683-be3d76c8958f">IDiscFormat2RawCD::get_BufferUnderrunFreeDisabled</a>
 

 

