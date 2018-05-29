---
UID: NF:winsync.IRecoverableError.GetStage
title: IRecoverableError::GetStage
author: windows-sdk-content
description: Gets the stage in the synchronization session when the error occurred.
old-location: winsync\irecoverableerror_getstage.htm
old-project: winsync
ms.assetid: 4ddfb151-37f1-4df2-827a-11bc6f23ace6
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetStage, GetStage method [Windows Sync], GetStage method [Windows Sync],IRecoverableError interface, IRecoverableError interface [Windows Sync],GetStage method, IRecoverableError.GetStage, IRecoverableError::GetStage, winsync.irecoverableerror_getstage, winsync/IRecoverableError::GetStage
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
-	IRecoverableError.GetStage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IRecoverableError::GetStage


## -description


Gets the stage in the synchronization session when the error occurred.


## -parameters




### -param pStage [out]

Returns the stage in the synchronization session when the error occurred.


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




<a href="https://msdn.microsoft.com/a8b8a84a-6083-4696-bef1-46145a4d71c8">IRecoverableError Interface</a>
 

 

