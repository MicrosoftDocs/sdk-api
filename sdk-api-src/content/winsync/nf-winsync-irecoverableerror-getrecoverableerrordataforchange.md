---
UID: NF:winsync.IRecoverableError.GetRecoverableErrorDataForChange
title: IRecoverableError::GetRecoverableErrorDataForChange (winsync.h)
author: windows-sdk-content
description: Gets additional data about the recoverable error.
old-location: winsync\irecoverableerror_getrecoverableerrordataforchange.htm
tech.root: winsync
ms.assetid: e6fbc99f-ae01-4f5e-b22c-bd802520ae39
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecoverableErrorDataForChange, GetRecoverableErrorDataForChange method [Windows Sync], GetRecoverableErrorDataForChange method [Windows Sync],IRecoverableError interface, IRecoverableError interface [Windows Sync],GetRecoverableErrorDataForChange method, IRecoverableError.GetRecoverableErrorDataForChange, IRecoverableError::GetRecoverableErrorDataForChange, winsync.irecoverableerror_getrecoverableerrordataforchange, winsync/IRecoverableError::GetRecoverableErrorDataForChange
ms.topic: method
f1_keywords: 
 - "winsync/IRecoverableError.GetRecoverableErrorDataForChange"
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
 - IRecoverableError.GetRecoverableErrorDataForChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-irecoverableerror">IRecoverableError Interface</a>
 

 

