---
UID: NF:imapi2.IDiscFormat2Data.put_BufferUnderrunFreeDisabled
title: IDiscFormat2Data::put_BufferUnderrunFreeDisabled
author: windows-driver-content
description: Determines if Buffer Underrun Free recording is enabled.
old-location: imapi\idiscformat2data_put_bufferunderrunfreedisabled.htm
old-project: imapi
ms.assetid: 32d05abe-c434-4a87-b6ee-961a999321c5
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],put_BufferUnderrunFreeDisabled method, IDiscFormat2Data.put_BufferUnderrunFreeDisabled, IDiscFormat2Data::put_BufferUnderrunFreeDisabled, imapi.idiscformat2data_put_bufferunderrunfreedisabled, imapi2/IDiscFormat2Data::put_BufferUnderrunFreeDisabled, put_BufferUnderrunFreeDisabled, put_BufferUnderrunFreeDisabled method [IMAPI], put_BufferUnderrunFreeDisabled method [IMAPI],IDiscFormat2Data interface
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
-	IDiscFormat2Data.put_BufferUnderrunFreeDisabled
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2Data::put_BufferUnderrunFreeDisabled


## -description


Determines if Buffer Underrun Free recording is enabled. <div class="alert"><b>Note</b>  This method  is only applicable to CDR/RW and DVD+/-R media formats.</div>
<div> </div>



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
<dt><b>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
There is currently a write operation in progress.

Value: 0xC0AA0400

</td>
</tr>
</table>
 




## -remarks



Buffer underrun can be an issue if the data stream does not enter the buffer fast enough to keep the device continuously writing. In turn, the stop and start action of writing can cause data on the disc to be unusable. Buffer Underrun Free (BUF) recording allows the laser to start and stop without damaging data already written to the disc. Disabling of BUF recording is possible only on CD-R/RW media.




## -see-also




<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data,IDiscFormat2Data::get_BufferUnderrunFreeDisabled</a>
 

 

