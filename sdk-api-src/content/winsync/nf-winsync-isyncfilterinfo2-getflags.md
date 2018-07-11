---
UID: NF:winsync.ISyncFilterInfo2.GetFlags
title: ISyncFilterInfo2::GetFlags
author: windows-sdk-content
description: Gets the flags that specify additional information about the filter information object.
old-location: winsync\isyncfilterinfo2_getflags.htm
old-project: winsync
ms.assetid: cad60957-9d16-4564-b63e-be8e188caecc
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetFlags, GetFlags method [Windows Sync], GetFlags method [Windows Sync],ISyncFilterInfo2 interface, ISyncFilterInfo2 interface [Windows Sync],GetFlags method, ISyncFilterInfo2.GetFlags, ISyncFilterInfo2::GetFlags, winsync.isyncfilterinfo2_getflags, winsync/ISyncFilterInfo2::GetFlags
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncFilterInfo2.GetFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncFilterInfo2::GetFlags


## -description


Gets the flags that specify additional information about the filter information object.


## -parameters




### -param pdwFlags [out]

Gets the flags that specify additional information about the filter information object. This will be one of the <b>SYNC_FILTER_INFO_FLAG</b> values (See Remarks).


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
 




## -remarks



The following table describes the flags that specify information about an <a href="https://msdn.microsoft.com/89a6d1c4-691d-4356-9ef5-1364b5a7507d">ISyncFilterInfo</a> object.

<table>
<tr>
<th>SYNC_FILTER_INFO_FLAG value</th>
<th>Description </th>
</tr>
<tr>
<td><b>SYNC_FILTER_INFO_FLAG_ITEM_LIST</b></td>
<td>This flag indicates that the set of items synchronized is restricted by an item filter.


</td>
</tr>
<tr>
<td><b>SYNC_FILTER_INFO_FLAG_CHANGE_UNIT_LIST</b></td>
<td>An <a href="https://msdn.microsoft.com/fd379fc6-22e5-4165-b4e6-480bc65cccb3">IChangeUnitListFilterInfo</a> object specifies that changes apply only to a subset of the change units that are defined for the scope.
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fd379fc6-22e5-4165-b4e6-480bc65cccb3">IChangeUnitListFilterInfo Interface</a>



<a href="https://msdn.microsoft.com/89a6d1c4-691d-4356-9ef5-1364b5a7507d">ISyncFilterInfo Interface</a>



<a href="https://msdn.microsoft.com/b1ffc6a7-ca82-4ce6-b7ac-c4c39c59891d">ISyncFilterInfo2 Interface</a>
 

 

