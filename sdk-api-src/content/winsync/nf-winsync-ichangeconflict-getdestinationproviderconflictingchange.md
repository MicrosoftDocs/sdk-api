---
UID: NF:winsync.IChangeConflict.GetDestinationProviderConflictingChange
title: IChangeConflict::GetDestinationProviderConflictingChange (winsync.h)
description: Gets the change metadata from the destination provider.
helpviewer_keywords: ["GetDestinationProviderConflictingChange","GetDestinationProviderConflictingChange method [Windows Sync]","GetDestinationProviderConflictingChange method [Windows Sync]","IChangeConflict interface","IChangeConflict interface [Windows Sync]","GetDestinationProviderConflictingChange method","IChangeConflict.GetDestinationProviderConflictingChange","IChangeConflict::GetDestinationProviderConflictingChange","winsync.ichangeconflict_getdestinationproviderconflictingchange","winsync/IChangeConflict::GetDestinationProviderConflictingChange"]
old-location: winsync\ichangeconflict_getdestinationproviderconflictingchange.htm
tech.root: winsync
ms.assetid: 4624f92a-8455-4490-a256-9cf849626844
ms.date: 12/05/2018
ms.keywords: GetDestinationProviderConflictingChange, GetDestinationProviderConflictingChange method [Windows Sync], GetDestinationProviderConflictingChange method [Windows Sync],IChangeConflict interface, IChangeConflict interface [Windows Sync],GetDestinationProviderConflictingChange method, IChangeConflict.GetDestinationProviderConflictingChange, IChangeConflict::GetDestinationProviderConflictingChange, winsync.ichangeconflict_getdestinationproviderconflictingchange, winsync/IChangeConflict::GetDestinationProviderConflictingChange
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
 - IChangeConflict::GetDestinationProviderConflictingChange
 - winsync/IChangeConflict::GetDestinationProviderConflictingChange
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
 - IChangeConflict.GetDestinationProviderConflictingChange
---

# IChangeConflict::GetDestinationProviderConflictingChange


## -description

Gets the change metadata from the destination provider.

## -parameters

### -param ppConflictingChange [out]

Returns the change metadata from the destination provider.

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
<dt><b>SYNC_E_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The change from the destination provider does not exist.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeconflict">IChangeConflict Interface</a>