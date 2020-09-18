---
UID: NF:winsync.IRecoverableError.GetProvider
title: IRecoverableError::GetProvider (winsync.h)
description: Gets the role of the provider that skipped the item change.
helpviewer_keywords: ["GetProvider","GetProvider method [Windows Sync]","GetProvider method [Windows Sync]","IRecoverableError interface","IRecoverableError interface [Windows Sync]","GetProvider method","IRecoverableError.GetProvider","IRecoverableError::GetProvider","winsync.irecoverableerror_getprovider","winsync/IRecoverableError::GetProvider"]
old-location: winsync\irecoverableerror_getprovider.htm
tech.root: winsync
ms.assetid: 48ecfc21-ab30-45c7-879b-c2487288419f
ms.date: 12/05/2018
ms.keywords: GetProvider, GetProvider method [Windows Sync], GetProvider method [Windows Sync],IRecoverableError interface, IRecoverableError interface [Windows Sync],GetProvider method, IRecoverableError.GetProvider, IRecoverableError::GetProvider, winsync.irecoverableerror_getprovider, winsync/IRecoverableError::GetProvider
req.header: winsync.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRecoverableError::GetProvider
 - winsync/IRecoverableError::GetProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IRecoverableError.GetProvider
---

# IRecoverableError::GetProvider


## -description

Gets the role of the provider that skipped the item change.

## -parameters

### -param pProviderRole [out]

Returns the role of the provider that skipped the item change.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-irecoverableerror">IRecoverableError Interface</a>