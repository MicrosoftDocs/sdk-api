---
UID: NF:imapi2.IWriteEngine2.put_BytesPerSector
title: IWriteEngine2::put_BytesPerSector
author: windows-sdk-content
description: Sets the number of bytes to use for each sector during writing.
old-location: imapi\iwriteengine2_put_bytespersector.htm
tech.root: imapi
ms.assetid: aac64c0a-4304-4a20-822e-4aa247d3d9e8
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWriteEngine2 interface [IMAPI],put_BytesPerSector method, IWriteEngine2.put_BytesPerSector, IWriteEngine2::put_BytesPerSector, imapi.iwriteengine2_put_bytespersector, imapi2/IWriteEngine2::put_BytesPerSector, put_BytesPerSector, put_BytesPerSector method [IMAPI], put_BytesPerSector method [IMAPI],IWriteEngine2 interface
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
 - IWriteEngine2.put_BytesPerSector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWriteEngine2::put_BytesPerSector


## -description


Sets the number of bytes to use for each sector during writing. 


## -parameters




### -param value [in]

Number of bytes to use for each sector during writing. The minimum size is 1 byte and the maximum is MAXLONG bytes. Typically, this value is 2,048 bytes for CD media, although any arbitrary size is supported (such as 2352 or 2448). This value is limited to the <a href="https://msdn.microsoft.com/6bf25c61-e87c-4ccf-a989-1c2715709d4a">IDiscRecorder2Ex::GetMaximumPageAlignedTransferSize</a>, which is typically 65,536 (64K) bytes.


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



You must specify a logical block size.




## -see-also




<a href="https://msdn.microsoft.com/89e7526f-2b9b-4f37-b537-5046a0ac283d">IWriteEngine2</a>



<a href="https://msdn.microsoft.com/ee48368c-e9bc-4ac7-97cf-a2bdc2a05d22">IWriteEngine2::get_BytesPerSector</a>



<a href="https://msdn.microsoft.com/7e6a5f41-328d-47b3-ba43-900e524cf51a">IWriteEngine2::get_EndingSectorsPerSecond</a>



<a href="https://msdn.microsoft.com/335da519-7378-469d-83dc-7c6a265fe67b">IWriteEngine2::get_StartingSectorsPerSecond</a>



<a href="https://msdn.microsoft.com/7060578d-c6d5-4155-9ab8-7185bde38f64">IWriteEngine2::put_EndingSectorsPerSecond</a>



<a href="https://msdn.microsoft.com/80d6efdd-c3ce-4c6b-9bc2-7ad34c1dfb5e">IWriteEngine2::put_StartingSectorsPerSecond</a>
 

 

