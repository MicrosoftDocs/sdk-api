---
UID: NF:winsync.ISyncChange.GetRootItemId
title: ISyncChange::GetRootItemId
author: windows-sdk-content
description: Gets the ID of the changed item.
old-location: winsync\isyncchange_getrootitemid.htm
old-project: winsync
ms.assetid: 775868d5-8cab-431a-913b-b22b2d516f0d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetRootItemId, GetRootItemId method [Windows Sync], GetRootItemId method [Windows Sync],ISyncChange interface, ISyncChange interface [Windows Sync],GetRootItemId method, ISyncChange.GetRootItemId, ISyncChange::GetRootItemId, winsync.isyncchange_getrootitemid, winsync/ISyncChange::GetRootItemId
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISyncChange.GetRootItemId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChange::GetRootItemId


## -description


Gets the ID of the changed item.


## -parameters




### -param pbRootItemId [in, out]

Returns the ID of the item.


### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbRootItemId</i>. Returns the number of bytes required to retrieve the ID when <i>pbRootItemId</i> is too small, or returns the number of bytes written.


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
<i>pbRootItemId</i> is too small. In this case, the required number of bytes is returned in <i>pcbIdSize</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0cd29977-8d02-4a1e-b63f-783cc10021ee">ISyncChange Interface</a>
 

 

