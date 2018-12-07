---
UID: NF:imapi2.IWriteEngine2.get_StartingSectorsPerSecond
title: IWriteEngine2::get_StartingSectorsPerSecond
author: windows-sdk-content
description: Retrieves the estimated number of sectors per second that the recording device can write to the media at the start of the writing process.
old-location: imapi\iwriteengine2_get_startingsectorspersecond.htm
tech.root: imapi
ms.assetid: 335da519-7378-469d-83dc-7c6a265fe67b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWriteEngine2 interface [IMAPI],get_StartingSectorsPerSecond method, IWriteEngine2.get_StartingSectorsPerSecond, IWriteEngine2::get_StartingSectorsPerSecond, get_StartingSectorsPerSecond, get_StartingSectorsPerSecond method [IMAPI], get_StartingSectorsPerSecond method [IMAPI],IWriteEngine2 interface, imapi.iwriteengine2_get_startingsectorspersecond, imapi2/IWriteEngine2::get_StartingSectorsPerSecond
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
 - IWriteEngine2.get_StartingSectorsPerSecond
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWriteEngine2::get_StartingSectorsPerSecond


## -description


Retrieves the estimated number of sectors per second that the recording device can write to the media at the start of the writing process.


## -parameters




### -param value [out]

Approximate number of sectors per second that the recording device can write to the media at the start of the writing process.

A value of -1 indicates maximum speed.


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



<a href="https://msdn.microsoft.com/ee48368c-e9bc-4ac7-97cf-a2bdc2a05d22">IWriteEngine2::get_BytesPerSector</a>



<a href="https://msdn.microsoft.com/7e6a5f41-328d-47b3-ba43-900e524cf51a">IWriteEngine2::get_EndingSectorsPerSecond</a>



<a href="https://msdn.microsoft.com/aac64c0a-4304-4a20-822e-4aa247d3d9e8">IWriteEngine2::put_BytesPerSector</a>



<a href="https://msdn.microsoft.com/7060578d-c6d5-4155-9ab8-7185bde38f64">IWriteEngine2::put_EndingSectorsPerSecond</a>



<a href="https://msdn.microsoft.com/80d6efdd-c3ce-4c6b-9bc2-7ad34c1dfb5e">IWriteEngine2::put_StartingSectorsPerSecond</a>
 

 

