---
UID: NF:shobjidl_core.ITransferDestination.Advise
title: ITransferDestination::Advise
author: windows-sdk-content
description: Sets up an advisory connection for notifications on the status of file operations.
old-location: shell\ITransferDestination_Advise.htm
tech.root: shell
ms.assetid: e25040dd-bb51-45cc-99fb-9113e26d0baa
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],ITransferDestination interface, ITransferDestination interface [Windows Shell],Advise method, ITransferDestination.Advise, ITransferDestination::Advise, _shell_ITransferDestination_Advise, shell.ITransferDestination_Advise, shobjidl_core/ITransferDestination::Advise
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - ITransferDestination.Advise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



