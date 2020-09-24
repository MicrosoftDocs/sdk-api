---
UID: NF:slpublic.SLDepositMigrationBlob
title: SLDepositMigrationBlob function (slpublic.h)
description: Deposits licensing information previously collected and gathered using the SLGatherMigrationBlob function.
helpviewer_keywords: ["SLDepositMigrationBlob","SLDepositMigrationBlob function [Security]","security.sldepositmigrationblob","slpublic/SLDepositMigrationBlob"]
old-location: security\sldepositmigrationblob.htm
tech.root: security
ms.assetid: 0fe3e466-c4df-4c11-9689-1002045df791
ms.date: 12/05/2018
ms.keywords: SLDepositMigrationBlob, SLDepositMigrationBlob function [Security], security.sldepositmigrationblob, slpublic/SLDepositMigrationBlob
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
 - SLDepositMigrationBlob
 - slpublic/SLDepositMigrationBlob
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
 - SLDepositMigrationBlob
---

# SLDepositMigrationBlob function


## -description

Deposits licensing information previously collected and gathered using the <a href="/windows/desktop/api/slpublic/nf-slpublic-slgathermigrationblob">SLGatherMigrationBlob</a> function.

## -parameters

### -param hFile [in]

Type: <b>HANDLE</b>

The file handle for the licensing state BLOB.

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