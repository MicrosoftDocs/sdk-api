---
UID: NF:slpublic.SLDepositMigrationBlob
title: SLDepositMigrationBlob function
author: windows-sdk-content
description: Deposits licensing information previously collected and gathered using the SLGatherMigrationBlob function.
old-location: security\sldepositmigrationblob.htm
old-project: secslapi
ms.assetid: 0fe3e466-c4df-4c11-9689-1002045df791
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SLDepositMigrationBlob, SLDepositMigrationBlob function [Security], security.sldepositmigrationblob, slpublic/SLDepositMigrationBlob
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: slpublic.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SL_ACTIVATION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slc.dll
api_name:
 - SLDepositMigrationBlob
product: Windows
targetos: Windows
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SLDepositMigrationBlob function


## -description


Deposits licensing information previously collected and gathered using the <a href="https://msdn.microsoft.com/490a5dbd-8c4b-4b25-ae21-f5f58b97a58f">SLGatherMigrationBlob</a> function.


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
 



