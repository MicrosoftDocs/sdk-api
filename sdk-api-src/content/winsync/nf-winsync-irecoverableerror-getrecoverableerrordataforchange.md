---
UID: NF:winsync.IRecoverableError.GetRecoverableErrorDataForChange
title: IRecoverableError::GetRecoverableErrorDataForChange
author: windows-sdk-content
description: Gets additional data about the recoverable error.
old-location: winsync\irecoverableerror_getrecoverableerrordataforchange.htm
old-project: winsync
ms.assetid: e6fbc99f-ae01-4f5e-b22c-bd802520ae39
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetRecoverableErrorDataForChange, GetRecoverableErrorDataForChange method [Windows Sync], GetRecoverableErrorDataForChange method [Windows Sync],IRecoverableError interface, IRecoverableError interface [Windows Sync],GetRecoverableErrorDataForChange method, IRecoverableError.GetRecoverableErrorDataForChange, IRecoverableError::GetRecoverableErrorDataForChange, winsync.irecoverableerror_getrecoverableerrordataforchange, winsync/IRecoverableError::GetRecoverableErrorDataForChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: winsync.h
req.include-header: 
req.redist: 
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
 - IRecoverableError.GetRecoverableErrorDataForChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IRecoverableError::GetRecoverableErrorDataForChange


## -description


Gets additional data about the recoverable error.


## -parameters




### -param phrError [out]

Returns the error code that is associated with the error that prevented the change unit data from being applied.


### -param ppErrorData [out]

Returns additional information about the error.


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
 

 

