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

# SLGatherMigrationBlob function


## -description


Gathers licensing information for the provided file handle. This licensing information  
	can later be applied or deposited using the <a href="https://msdn.microsoft.com/0fe3e466-c4df-4c11-9689-1002045df791">SLDepositMigrationBlob</a> function.


## -parameters




### -param bMigratableOnly [in]

Type: <b>BOOL</b>

<b>TRUE</b> if only data that can be migrated should be gathered; <b>FALSE</b> otherwise.


### -param pwszEncryptorUri [in, optional]

Type: <b>LPCWSTR</b>

The URI of the encrypting session key used to encrypt      
		any sensitive data in the output BLOB. Only valid values are <b>NULL</b> and <b>SL_DEFAULT_MIGRATION_ENCRYPTOR_URI</b>,     
		which both refer to the same key.


### -param hFile [in]

Type: <b>HANDLE</b>

The handle to the file where the licensing state BLOB should be written.


## -returns



Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise,  it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
<dt>0x80070005</dt>
</dl>
</td>
<td width="60%">
Access denied (API requires admin privileges).

</td>
</tr>
</table>
 



