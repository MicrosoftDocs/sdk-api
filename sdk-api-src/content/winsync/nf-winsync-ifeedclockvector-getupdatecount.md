---
UID: NF:winsync.IFeedClockVector.GetUpdateCount
title: IFeedClockVector::GetUpdateCount (winsync.h)
description: Gets the number of updates that have been made to the FeedSync item.
helpviewer_keywords: ["GetUpdateCount","GetUpdateCount method [Windows Sync]","GetUpdateCount method [Windows Sync]","IFeedClockVector interface","IFeedClockVector interface [Windows Sync]","GetUpdateCount method","IFeedClockVector.GetUpdateCount","IFeedClockVector::GetUpdateCount","winsync.ifeedclockvector_getupdatecount","winsync/IFeedClockVector::GetUpdateCount"]
old-location: winsync\ifeedclockvector_getupdatecount.htm
tech.root: winsync
ms.assetid: a8cf6b0f-2049-4047-b72d-34530ae82605
ms.date: 12/05/2018
ms.keywords: GetUpdateCount, GetUpdateCount method [Windows Sync], GetUpdateCount method [Windows Sync],IFeedClockVector interface, IFeedClockVector interface [Windows Sync],GetUpdateCount method, IFeedClockVector.GetUpdateCount, IFeedClockVector::GetUpdateCount, winsync.ifeedclockvector_getupdatecount, winsync/IFeedClockVector::GetUpdateCount
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
 - IFeedClockVector::GetUpdateCount
 - winsync/IFeedClockVector::GetUpdateCount
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
 - IFeedClockVector.GetUpdateCount
---

# IFeedClockVector::GetUpdateCount


## -description

Gets the number of updates that have been made to the FeedSync item.

## -parameters

### -param pdwUpdateCount [out]

Returns the number of updates that have been made to the FeedSync item. This value corresponds to the <b>updates</b> attribute of the FeedSync item.

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

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ifeedclockvector">IFeedClockVector Interface</a>