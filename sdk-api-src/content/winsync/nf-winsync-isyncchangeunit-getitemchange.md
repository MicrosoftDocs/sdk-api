---
UID: NF:winsync.ISyncChangeUnit.GetItemChange
title: ISyncChangeUnit::GetItemChange (winsync.h)
author: windows-sdk-content
description: Gets the item change that contains this change unit change.
old-location: winsync\isyncchangeunit_getitemchange.htm
tech.root: winsync
ms.assetid: d28b4eb0-ddd2-4abf-9183-4d39b728923b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetItemChange, GetItemChange method [Windows Sync], GetItemChange method [Windows Sync],ISyncChangeUnit interface, ISyncChangeUnit interface [Windows Sync],GetItemChange method, ISyncChangeUnit.GetItemChange, ISyncChangeUnit::GetItemChange, winsync.isyncchangeunit_getitemchange, winsync/ISyncChangeUnit::GetItemChange
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncChangeUnit.GetItemChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncChangeUnit::GetItemChange


## -description


Gets the item change that contains this change unit change.


## -parameters




### -param ppSyncChange [out]

Returns the item change that contains this change unit change.


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




<a href="https://msdn.microsoft.com/6c889a78-1a50-47b5-8e49-4aba741c0be0">ISyncChangeUnit Interface</a>
 

 

