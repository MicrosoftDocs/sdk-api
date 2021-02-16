---
UID: NF:winsync.IRecoverableErrorData.Initialize
title: IRecoverableErrorData::Initialize (winsync.h)
description: Initializes the object by using the specified display name of the item that caused the error and a description of the error.
helpviewer_keywords: ["IRecoverableErrorData interface [Windows Sync]","Initialize method","IRecoverableErrorData.Initialize","IRecoverableErrorData::Initialize","Initialize","Initialize method [Windows Sync]","Initialize method [Windows Sync]","IRecoverableErrorData interface","winsync.irecoverableerrordata_initialize","winsync/IRecoverableErrorData::Initialize"]
old-location: winsync\irecoverableerrordata_initialize.htm
tech.root: winsync
ms.assetid: df34b3ee-fc78-47ca-8916-ee4a81110628
ms.date: 12/05/2018
ms.keywords: IRecoverableErrorData interface [Windows Sync],Initialize method, IRecoverableErrorData.Initialize, IRecoverableErrorData::Initialize, Initialize, Initialize method [Windows Sync], Initialize method [Windows Sync],IRecoverableErrorData interface, winsync.irecoverableerrordata_initialize, winsync/IRecoverableErrorData::Initialize
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
 - IRecoverableErrorData::Initialize
 - winsync/IRecoverableErrorData::Initialize
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
 - IRecoverableErrorData.Initialize
---

# IRecoverableErrorData::Initialize


## -description

Initializes the object by using the specified display name of the item that caused the error and a description of the error.

## -parameters

### -param pcszItemDisplayName [in]

The display name of the item that caused the error.

### -param pcszErrorDescription [in]

The description of the error.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
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