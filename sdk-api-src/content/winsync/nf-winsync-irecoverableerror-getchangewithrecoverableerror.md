---
UID: NF:winsync.IRecoverableError.GetChangeWithRecoverableError
title: IRecoverableError::GetChangeWithRecoverableError (winsync.h)
author: windows-sdk-content
description: Gets the item change that caused the error.
old-location: winsync\irecoverableerror_getchangewithrecoverableerror.htm
tech.root: winsync
ms.assetid: c7ddc479-1428-43d9-9a26-4166cf4eec3d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetChangeWithRecoverableError, GetChangeWithRecoverableError method [Windows Sync], GetChangeWithRecoverableError method [Windows Sync],IRecoverableError interface, IRecoverableError interface [Windows Sync],GetChangeWithRecoverableError method, IRecoverableError.GetChangeWithRecoverableError, IRecoverableError::GetChangeWithRecoverableError, winsync.irecoverableerror_getchangewithrecoverableerror, winsync/IRecoverableError::GetChangeWithRecoverableError
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
 - IRecoverableError.GetChangeWithRecoverableError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRecoverableError::GetChangeWithRecoverableError


## -description


Gets the item change that caused the error.


## -parameters




### -param ppChangeWithRecoverableError [out]

Returns the item change that caused the error.


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
 

 

