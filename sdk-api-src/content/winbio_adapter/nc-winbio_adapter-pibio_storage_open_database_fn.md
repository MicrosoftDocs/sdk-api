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

# PIBIO_STORAGE_OPEN_DATABASE_FN callback function


## -description


Called by the Windows Biometric Framework to open a database.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param DatabaseId [in]

Pointer to a GUID that uniquely identifies the database. This is the same GUID used to register the database in the registry.


### -param FilePath [in]

Pointer to a <b>NULL</b>-terminated Unicode string that contains the fully qualified file path for the database.


### -param ConnectString [in]

Pointer to a <b>NULL</b>-terminated Unicode connection string for the database.


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
<dt><b><b>WINBIO_E_DATABASE_CANT_CREATE</b></b></dt>
</dl>
</td>
<td width="60%">
The database cannot be created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DATABASE_CANT_FIND</b></b></dt>
</dl>
</td>
<td width="60%">
The specified database cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DATABASE_LOCKED</b></b></dt>
</dl>
</td>
<td width="60%">
The database is currently locked by another application and cannot be opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DATABASE_CANT_OPEN</b></b></dt>
</dl>
</td>
<td width="60%">
An unspecified problem has caused the request to fail.

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



<a href="https://msdn.microsoft.com/ddb8d0b8-e975-4ee2-bb8c-423b1304c467">StorageAdapterCloseDatabase</a>



<a href="https://msdn.microsoft.com/7b9e034e-51d4-4209-9092-14e21e9fff3c">StorageAdapterCreateDatabase</a>



<a href="https://msdn.microsoft.com/c1fc2f3f-034b-4546-aeee-1d1a38695793">StorageAdapterEraseDatabase</a>
 

 

