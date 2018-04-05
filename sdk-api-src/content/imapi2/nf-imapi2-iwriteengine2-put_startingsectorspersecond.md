---
UID: NF:imapi2.IWriteEngine2.put_StartingSectorsPerSecond
title: IWriteEngine2::put_StartingSectorsPerSecond method
author: windows-driver-content
description: Sets the estimated number of sectors per second that the recording device can write to the media at the start of the writing process.
old-location: imapi\iwriteengine2_put_startingsectorspersecond.htm
old-project: imapi
ms.assetid: 80d6efdd-c3ce-4c6b-9bc2-7ad34c1dfb5e
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IWriteEngine2, IWriteEngine2 interface [IMAPI], put_StartingSectorsPerSecond method, IWriteEngine2::put_StartingSectorsPerSecond, imapi.iwriteengine2_put_startingsectorspersecond, imapi2/IWriteEngine2::put_StartingSectorsPerSecond, put_StartingSectorsPerSecond method [IMAPI], put_StartingSectorsPerSecond method [IMAPI], IWriteEngine2 interface, put_StartingSectorsPerSecond,IWriteEngine2.put_StartingSectorsPerSecond
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
-	IWriteEngine2.put_StartingSectorsPerSecond
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWriteEngine2::put_StartingSectorsPerSecond method


## -description


Sets the estimated number of sectors per second that the recording device can write to the media at the start of the writing process.


## -parameters




### -param value [in]

Approximate number of sectors per second that the recording device can write to the media at the start of the writing process. The default is -1 for maximum speed.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

Value: 0x80070057

</td>
</tr>
</table>
 




## -remarks



This is used to optimize sleep time in the write engine.




## -see-also




<a href="https://msdn.microsoft.com/89e7526f-2b9b-4f37-b537-5046a0ac283d">IWriteEngine2</a>



<a href="https://msdn.microsoft.com/ee48368c-e9bc-4ac7-97cf-a2bdc2a05d22">IWriteEngine2::get_BytesPerSector</a>



<a href="https://msdn.microsoft.com/7e6a5f41-328d-47b3-ba43-900e524cf51a">IWriteEngine2::get_EndingSectorsPerSecond</a>



<a href="https://msdn.microsoft.com/335da519-7378-469d-83dc-7c6a265fe67b">IWriteEngine2::get_StartingSectorsPerSecond</a>



<a href="https://msdn.microsoft.com/aac64c0a-4304-4a20-822e-4aa247d3d9e8">IWriteEngine2::put_BytesPerSector</a>



<a href="https://msdn.microsoft.com/7060578d-c6d5-4155-9ab8-7185bde38f64">IWriteEngine2::put_EndingSectorsPerSecond</a>
 

 

