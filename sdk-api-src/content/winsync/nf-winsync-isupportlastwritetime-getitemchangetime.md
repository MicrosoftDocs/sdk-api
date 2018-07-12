---
UID: NF:winsync.ISupportLastWriteTime.GetItemChangeTime
title: ISupportLastWriteTime::GetItemChangeTime
author: windows-sdk-content
description: Gets the date and time when the specified item was last changed.
old-location: winsync\isupportlastwritetime_getitemchangetime.htm
old-project: winsync
ms.assetid: 15cbd398-81d9-4ea6-bfe4-1bf00510b419
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetItemChangeTime, GetItemChangeTime method [Windows Sync], GetItemChangeTime method [Windows Sync],ISupportLastWriteTime interface, ISupportLastWriteTime interface [Windows Sync],GetItemChangeTime method, ISupportLastWriteTime.GetItemChangeTime, ISupportLastWriteTime::GetItemChangeTime, winsync.isupportlastwritetime_getitemchangetime, winsync/ISupportLastWriteTime::GetItemChangeTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - ISupportLastWriteTime.GetItemChangeTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/b95e2b75-add7-4cdd-b18a-21918e9c8c08">ISupportLastWriteTime Interface</a>
 

 

