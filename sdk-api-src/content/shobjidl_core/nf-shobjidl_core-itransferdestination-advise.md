---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ITransferDestination::Advise


## -description


Sets up an advisory connection for notifications on the status of file operations.


## -parameters




### -param psink [in]

Type: <b><a href="https://msdn.microsoft.com/70866a03-2b22-4518-a9e6-2f06edaa4b5d">ITransferAdviseSink</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/70866a03-2b22-4518-a9e6-2f06edaa4b5d">ITransferAdviseSink</a> notification interface to update the calling application using methods on this interface.


### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to a returned token that uniquely identifies this connection. The calling application uses this token later to delete the connection by passing it to the <a href="https://msdn.microsoft.com/ecc3d32b-50cb-48d3-90c2-aba4614f863d">ITransferDestination::Unadvise</a> method. If the connection is not successfully established, this value is zero.


## -returns



Type: <b>HRESULT</b>

Any HRESULTs other than listed indicate a failure.

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
The Interface successfully associated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The handler can only handle one sink interface.

</td>
</tr>
</table>
 




## -remarks



Call <b>ITransferDestination::Advise</b> before calling any other <a href="https://msdn.microsoft.com/8d0049e0-e227-40ae-a282-cdc17f227e24">ITransferDestination</a> methods so the handler can callback for any errors that might occur. If not set, the handler should consider it an indication that no feedback is available and do the "default" operation.



