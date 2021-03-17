---
UID: NF:syncregistration.IEnumSyncProviderInfos.Next
title: IEnumSyncProviderInfos::Next (syncregistration.h)
description: Returns the next ISyncProviderInfo object.
helpviewer_keywords: ["IEnumSyncProviderInfos interface [Windows Sync]","Next method","IEnumSyncProviderInfos.Next","IEnumSyncProviderInfos::Next","Next","Next method [Windows Sync]","Next method [Windows Sync]","IEnumSyncProviderInfos interface","syncregistration/IEnumSyncProviderInfos::Next","winsync.ienumsyncproviderinfos_next"]
old-location: winsync\ienumsyncproviderinfos_next.htm
tech.root: winsync
ms.assetid: b56cacfd-9cfe-4f5a-a945-dca299e43497
ms.date: 12/05/2018
ms.keywords: IEnumSyncProviderInfos interface [Windows Sync],Next method, IEnumSyncProviderInfos.Next, IEnumSyncProviderInfos::Next, Next, Next method [Windows Sync], Next method [Windows Sync],IEnumSyncProviderInfos interface, syncregistration/IEnumSyncProviderInfos::Next, winsync.ienumsyncproviderinfos_next
req.header: syncregistration.h
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
 - IEnumSyncProviderInfos::Next
 - syncregistration/IEnumSyncProviderInfos::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - IEnumSyncProviderInfos.Next
---

# IEnumSyncProviderInfos::Next


## -description

Returns the next <b>ISyncProviderInfo</b> object.

## -parameters

### -param cInstances [in]

The number of <b>ISyncProviderInfo</b> objects to retrieve in the range of zero to 1.

### -param ppSyncProviderInfo [out]

Returns the next <i>pcFetched</i><b>ISyncProviderInfo</b> objects.

### -param pcFetched [out]

Returns the number of <b>ISyncProviderInfo</b> objects that are retrieved.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The requested number of objects was not available.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory available to return the next  <b>ISyncProviderInfo</b> object.

</td>
</tr>
</table>

## -remarks

This method will attempt to return the number of items specified by the <i>cInstances</i> parameter.  If the specified number of items is not available, <b>S_FALSE</b> will be returned, and <i>pcFetched</i> will contain the number of items that were able to be retrieved.

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-ienumsyncproviderinfos">IEnumSyncProviderInfos Interface</a>