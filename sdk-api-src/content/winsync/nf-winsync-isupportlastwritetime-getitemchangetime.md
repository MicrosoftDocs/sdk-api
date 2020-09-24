---
UID: NF:winsync.ISupportLastWriteTime.GetItemChangeTime
title: ISupportLastWriteTime::GetItemChangeTime (winsync.h)
description: Gets the date and time when the specified item was last changed.
helpviewer_keywords: ["GetItemChangeTime","GetItemChangeTime method [Windows Sync]","GetItemChangeTime method [Windows Sync]","ISupportLastWriteTime interface","ISupportLastWriteTime interface [Windows Sync]","GetItemChangeTime method","ISupportLastWriteTime.GetItemChangeTime","ISupportLastWriteTime::GetItemChangeTime","winsync.isupportlastwritetime_getitemchangetime","winsync/ISupportLastWriteTime::GetItemChangeTime"]
old-location: winsync\isupportlastwritetime_getitemchangetime.htm
tech.root: winsync
ms.assetid: 15cbd398-81d9-4ea6-bfe4-1bf00510b419
ms.date: 12/05/2018
ms.keywords: GetItemChangeTime, GetItemChangeTime method [Windows Sync], GetItemChangeTime method [Windows Sync],ISupportLastWriteTime interface, ISupportLastWriteTime interface [Windows Sync],GetItemChangeTime method, ISupportLastWriteTime.GetItemChangeTime, ISupportLastWriteTime::GetItemChangeTime, winsync.isupportlastwritetime_getitemchangetime, winsync/ISupportLastWriteTime::GetItemChangeTime
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ISupportLastWriteTime::GetItemChangeTime
 - winsync/ISupportLastWriteTime::GetItemChangeTime
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
 - ISupportLastWriteTime.GetItemChangeTime
---

# ISupportLastWriteTime::GetItemChangeTime


## -description

Gets the date and time when the specified item was last changed.

## -parameters

### -param pbItemId [in]

The ID of the item to look up.

### -param pullTimestamp [out]

The date and time when the specified item was last changed.

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
<dt><b>Provider-determined error codes</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isupportlastwritetime">ISupportLastWriteTime Interface</a>