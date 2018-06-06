---
UID: NF:winsync.ISyncChange.GetWorkEstimate
title: ISyncChange::GetWorkEstimate
author: windows-sdk-content
description: Gets the work estimate for this change.
old-location: winsync\isyncchange_getworkestimate.htm
old-project: winsync
ms.assetid: ba79bb88-bdeb-42be-88a9-1355fe048d10
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetWorkEstimate, GetWorkEstimate method [Windows Sync], GetWorkEstimate method [Windows Sync],ISyncChange interface, ISyncChange interface [Windows Sync],GetWorkEstimate method, ISyncChange.GetWorkEstimate, ISyncChange::GetWorkEstimate, winsync.isyncchange_getworkestimate, winsync/ISyncChange::GetWorkEstimate
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
 - ISyncChange.GetWorkEstimate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChange::GetWorkEstimate


## -description


Gets the work estimate for this change.


## -parameters




### -param pdwWork [out]

The work estimate for this change. The default value is zero.


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



The work estimate is a part of the total work that is estimated for the batch or the session.

The work estimate is only meaningful when the <b>ISyncChange</b> object represents a change from the source provider.




## -see-also




<a href="https://msdn.microsoft.com/0cd29977-8d02-4a1e-b63f-783cc10021ee">ISyncChange Interface</a>
 

 

