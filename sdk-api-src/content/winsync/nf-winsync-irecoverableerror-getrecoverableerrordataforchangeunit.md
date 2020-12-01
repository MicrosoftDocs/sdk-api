---
UID: NF:winsync.IRecoverableError.GetRecoverableErrorDataForChangeUnit
title: IRecoverableError::GetRecoverableErrorDataForChangeUnit (winsync.h)
description: Gets additional data about the recoverable error for a specified change unit.
helpviewer_keywords: ["GetRecoverableErrorDataForChangeUnit","GetRecoverableErrorDataForChangeUnit method [Windows Sync]","GetRecoverableErrorDataForChangeUnit method [Windows Sync]","IRecoverableError interface","IRecoverableError interface [Windows Sync]","GetRecoverableErrorDataForChangeUnit method","IRecoverableError.GetRecoverableErrorDataForChangeUnit","IRecoverableError::GetRecoverableErrorDataForChangeUnit","winsync.irecoverableerror_getrecoverableerrordataforchangeunit","winsync/IRecoverableError::GetRecoverableErrorDataForChangeUnit"]
old-location: winsync\irecoverableerror_getrecoverableerrordataforchangeunit.htm
tech.root: winsync
ms.assetid: 609ecdb0-b135-474f-b959-9ab6f427e5d6
ms.date: 12/05/2018
ms.keywords: GetRecoverableErrorDataForChangeUnit, GetRecoverableErrorDataForChangeUnit method [Windows Sync], GetRecoverableErrorDataForChangeUnit method [Windows Sync],IRecoverableError interface, IRecoverableError interface [Windows Sync],GetRecoverableErrorDataForChangeUnit method, IRecoverableError.GetRecoverableErrorDataForChangeUnit, IRecoverableError::GetRecoverableErrorDataForChangeUnit, winsync.irecoverableerror_getrecoverableerrordataforchangeunit, winsync/IRecoverableError::GetRecoverableErrorDataForChangeUnit
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
 - IRecoverableError::GetRecoverableErrorDataForChangeUnit
 - winsync/IRecoverableError::GetRecoverableErrorDataForChangeUnit
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
 - IRecoverableError.GetRecoverableErrorDataForChangeUnit
---

# IRecoverableError::GetRecoverableErrorDataForChangeUnit


## -description

Gets additional data about the recoverable error for a specified change unit.

## -parameters

### -param pChangeUnit [in]

The change unit that is associated with the error.

### -param phrError [out]

Returns the error code that is associated with the error that prevented the change unit data from being applied.

### -param ppErrorData [out]

Returns additional information about the error.

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