---
UID: NF:imapi2.IDiscFormat2Data.get_Recorder
title: IDiscFormat2Data::get_Recorder
author: windows-sdk-content
description: Retrieves the recording device to use for the write operation.
old-location: imapi\idiscformat2data_get_recorder.htm
old-project: imapi
ms.assetid: 313ba824-b54a-4b3a-a669-49067c71798d
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],get_Recorder method, IDiscFormat2Data.get_Recorder, IDiscFormat2Data::get_Recorder, get_Recorder, get_Recorder method [IMAPI], get_Recorder method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_get_recorder, imapi2/IDiscFormat2Data::get_Recorder
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscFormat2Data.get_Recorder
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2Data::get_Recorder


## -description


Retrieves the recording device to use for the write operation.


## -parameters




### -param value [out]

An <a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a> interface that identifies the recording device to use in the write operation.


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




<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/d8d1f6ec-09cb-4144-b44c-970555451aee">IDiscFormat2Data::put_Recorder</a>
 

 

