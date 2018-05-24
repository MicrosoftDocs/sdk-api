---
UID: NF:imapi2.IWriteEngine2.get_Recorder
title: IWriteEngine2::get_Recorder
author: windows-driver-content
description: Retrieves the recording device to use in the write operation.
old-location: imapi\iwriteengine2_get_recorder.htm
old-project: imapi
ms.assetid: f42c5289-0896-4e2f-902e-9c6bdbf23b40
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: IWriteEngine2 interface [IMAPI],get_Recorder method, IWriteEngine2.get_Recorder, IWriteEngine2::get_Recorder, get_Recorder, get_Recorder method [IMAPI], get_Recorder method [IMAPI],IWriteEngine2 interface, imapi.iwriteengine2_get_recorder, imapi2/IWriteEngine2::get_Recorder
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
-	IWriteEngine2.get_Recorder
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWriteEngine2::get_Recorder


## -description


Retrieves the recording device to use in the write operation.


## -parameters




### -param value [out]

An <a href="https://msdn.microsoft.com/37e65b57-ec53-405c-a7bd-34c2df15d5d7">IDiscRecorder2Ex</a> interface that identifies the recording device to use in the write operation.


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




<a href="https://msdn.microsoft.com/89e7526f-2b9b-4f37-b537-5046a0ac283d">IWriteEngine2</a>



<a href="https://msdn.microsoft.com/3ab46d99-7940-4ad0-9772-634de8c0d0ef">IWriteEngine2::put_Recorder</a>
 

 

