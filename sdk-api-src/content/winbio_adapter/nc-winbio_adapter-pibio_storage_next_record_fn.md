---
UID: NC:winbio_adapter.PIBIO_STORAGE_NEXT_RECORD_FN
title: PIBIO_STORAGE_NEXT_RECORD_FN
author: windows-sdk-content
description: Advances the result set cursor by one record.
old-location: secbiomet\storageadapternextrecord.htm
old-project: secbiomet
ms.assetid: e0025167-0778-474e-baca-ffc767822893
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: PIBIO_STORAGE_NEXT_RECORD_FN, PIBIO_STORAGE_NEXT_RECORD_FN callback, StorageAdapterNextRecord, StorageAdapterNextRecord callback function [Windows Biometric Framework API], secbiomet.storageadapternextrecord, winbio_adapter/StorageAdapterNextRecord
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - StorageAdapterNextRecord
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_STORAGE_NEXT_RECORD_FN callback function


## -description


Called by the Windows Biometric Framework or by an engine adapter to advance the result set cursor by one record.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


## -returns



If the function succeeds, it returns S_OK. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

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
The <i>Pipeline</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DATABASE_NO_RESULTS</b></b></dt>
</dl>
</td>
<td width="60%">
There are no records in the result set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DATABASE_NO_MORE_RECORDS</b></b></dt>
</dl>
</td>
<td width="60%">
The cursor is already on the last record.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>StorageContext</b> member of the pipeline object is <b>NULL</b> or the <b>FileHandle</b> member is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/736688c3-2c2c-4244-9f49-98ad0fe2d141">StorageAdapterFirstRecord</a>
 

 

