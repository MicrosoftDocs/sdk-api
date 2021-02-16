---
UID: NF:winsync.IRecoverableError.GetStage
title: IRecoverableError::GetStage (winsync.h)
description: Gets the stage in the synchronization session when the error occurred.
helpviewer_keywords: ["GetStage","GetStage method [Windows Sync]","GetStage method [Windows Sync]","IRecoverableError interface","IRecoverableError interface [Windows Sync]","GetStage method","IRecoverableError.GetStage","IRecoverableError::GetStage","winsync.irecoverableerror_getstage","winsync/IRecoverableError::GetStage"]
old-location: winsync\irecoverableerror_getstage.htm
tech.root: winsync
ms.assetid: 4ddfb151-37f1-4df2-827a-11bc6f23ace6
ms.date: 12/05/2018
ms.keywords: GetStage, GetStage method [Windows Sync], GetStage method [Windows Sync],IRecoverableError interface, IRecoverableError interface [Windows Sync],GetStage method, IRecoverableError.GetStage, IRecoverableError::GetStage, winsync.irecoverableerror_getstage, winsync/IRecoverableError::GetStage
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
 - IRecoverableError::GetStage
 - winsync/IRecoverableError::GetStage
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
 - IRecoverableError.GetStage
---

# IRecoverableError::GetStage


## -description

Gets the stage in the synchronization session when the error occurred.

## -parameters

### -param pStage [out]

Returns the stage in the synchronization session when the error occurred.

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