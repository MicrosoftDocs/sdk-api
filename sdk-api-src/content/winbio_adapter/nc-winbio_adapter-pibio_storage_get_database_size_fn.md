---
UID: NC:winbio_adapter.PIBIO_STORAGE_GET_DATABASE_SIZE_FN
title: PIBIO_STORAGE_GET_DATABASE_SIZE_FN
author: windows-sdk-content
description: Retrieves the database size and available space.
old-location: secbiomet\storageadaptergetdatabasesize.htm
old-project: SecBioMet
ms.assetid: 98e26b32-3e2a-40d9-8463-9bd7e93c636b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PIBIO_STORAGE_GET_DATABASE_SIZE_FN, PIBIO_STORAGE_GET_DATABASE_SIZE_FN callback, StorageAdapterGetDatabaseSize, StorageAdapterGetDatabaseSize callback function [Windows Biometric Framework API], secbiomet.storageadaptergetdatabasesize, winbio_adapter/StorageAdapterGetDatabaseSize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.redist: 
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
 - StorageAdapterGetDatabaseSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_STORAGE_GET_DATABASE_SIZE_FN callback function


## -description


Called by the Windows Biometric Framework to retrieve the database size and available space.


## -parameters




### -param Pipeline [in, out]

Pointer to a <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param AvailableRecordCount [out]

Pointer to a variable that receives the number of unused record slots in the database.


### -param TotalRecordCount [out]

Pointer to a variable that receives the number of valid records in the database.


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
A mandatory pointer argument is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>StorageContext</b> member of the pipeline object is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>
 

 

