---
UID: NF:winsync.IRecoverableErrorData.GetItemDisplayName
title: IRecoverableErrorData::GetItemDisplayName (winsync.h)
description: Gets the display name of the item that caused the error.
helpviewer_keywords: ["GetItemDisplayName","GetItemDisplayName method [Windows Sync]","GetItemDisplayName method [Windows Sync]","IRecoverableErrorData interface","IRecoverableErrorData interface [Windows Sync]","GetItemDisplayName method","IRecoverableErrorData.GetItemDisplayName","IRecoverableErrorData::GetItemDisplayName","winsync.irecoverableerrordata_getitemdisplayname","winsync/IRecoverableErrorData::GetItemDisplayName"]
old-location: winsync\irecoverableerrordata_getitemdisplayname.htm
tech.root: winsync
ms.assetid: 6b40d528-18dc-4924-959a-cde5f02d18b1
ms.date: 12/05/2018
ms.keywords: GetItemDisplayName, GetItemDisplayName method [Windows Sync], GetItemDisplayName method [Windows Sync],IRecoverableErrorData interface, IRecoverableErrorData interface [Windows Sync],GetItemDisplayName method, IRecoverableErrorData.GetItemDisplayName, IRecoverableErrorData::GetItemDisplayName, winsync.irecoverableerrordata_getitemdisplayname, winsync/IRecoverableErrorData::GetItemDisplayName
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
 - IRecoverableErrorData::GetItemDisplayName
 - winsync/IRecoverableErrorData::GetItemDisplayName
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
 - IRecoverableErrorData.GetItemDisplayName
---

# IRecoverableErrorData::GetItemDisplayName


## -description

Gets the display name of the item that caused the error.

## -parameters

### -param pszItemDisplayName [in, out]

Returns the display name of the item that caused the error.

### -param pcchItemDisplayName [in, out]

Specifies the number of characters in <i>pszItemDisplayName</i>. Returns the required number of characters for <i>pszItemDisplayName</i> when <i>pcchItemDisplayName</i> is too small; otherwise, returns the number of characters written.

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
<i>pszItemDisplayName</i> is too small. In this case, the required number of characters is returned in <i>pcchItemDisplayName</i>.

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