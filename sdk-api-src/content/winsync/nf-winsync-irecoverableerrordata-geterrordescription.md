---
UID: NF:winsync.IRecoverableErrorData.GetErrorDescription
title: IRecoverableErrorData::GetErrorDescription (winsync.h)
description: Gets the description of the error.
helpviewer_keywords: ["GetErrorDescription","GetErrorDescription method [Windows Sync]","GetErrorDescription method [Windows Sync]","IRecoverableErrorData interface","IRecoverableErrorData interface [Windows Sync]","GetErrorDescription method","IRecoverableErrorData.GetErrorDescription","IRecoverableErrorData::GetErrorDescription","winsync.irecoverableerrordata_geterrordescription","winsync/IRecoverableErrorData::GetErrorDescription"]
old-location: winsync\irecoverableerrordata_geterrordescription.htm
tech.root: winsync
ms.assetid: 9bd268aa-683d-4a77-966c-7cba0348d034
ms.date: 12/05/2018
ms.keywords: GetErrorDescription, GetErrorDescription method [Windows Sync], GetErrorDescription method [Windows Sync],IRecoverableErrorData interface, IRecoverableErrorData interface [Windows Sync],GetErrorDescription method, IRecoverableErrorData.GetErrorDescription, IRecoverableErrorData::GetErrorDescription, winsync.irecoverableerrordata_geterrordescription, winsync/IRecoverableErrorData::GetErrorDescription
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
 - IRecoverableErrorData::GetErrorDescription
 - winsync/IRecoverableErrorData::GetErrorDescription
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
 - IRecoverableErrorData.GetErrorDescription
---

# IRecoverableErrorData::GetErrorDescription


## -description

Gets the description of the error.

## -parameters

### -param pszErrorDescription [in, out]

Returns the description of the error.

### -param pcchErrorDescription [in, out]

Specifies the number of characters in <i>pszErrorDescription</i>. Returns the required number of characters for <i>pszErrorDescription</i> when <i>pcchErrorDescription</i> is too small; otherwise, returns the number of characters written.

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
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pszErrorDescription</i> is too small. In this case, the required number of characters is returned in <i>pcchErrorDescription</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Provider-determined error codes.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-irecoverableerrordata">IRecoverableErrorData Interface</a>