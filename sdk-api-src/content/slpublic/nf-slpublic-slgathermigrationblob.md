---
UID: NF:slpublic.SLGatherMigrationBlob
title: SLGatherMigrationBlob function (slpublic.h)
description: Gathers licensing information for the provided file handle. This licensing information can later be applied or deposited using the SLDepositMigrationBlob function.
helpviewer_keywords: ["SLGatherMigrationBlob","SLGatherMigrationBlob function [Security]","security.slgathermigrationblob","slpublic/SLGatherMigrationBlob"]
old-location: security\slgathermigrationblob.htm
tech.root: security
ms.assetid: 490a5dbd-8c4b-4b25-ae21-f5f58b97a58f
ms.date: 12/05/2018
ms.keywords: SLGatherMigrationBlob, SLGatherMigrationBlob function [Security], security.slgathermigrationblob, slpublic/SLGatherMigrationBlob
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SLGatherMigrationBlob
 - slpublic/SLGatherMigrationBlob
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slc.dll
api_name:
 - SLGatherMigrationBlob
---

# SLGatherMigrationBlob function


## -description

Gathers licensing information for the provided file handle. This licensing information  
	can later be applied or deposited using the <a href="/windows/desktop/api/slpublic/nf-slpublic-sldepositmigrationblob">SLDepositMigrationBlob</a> function.

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