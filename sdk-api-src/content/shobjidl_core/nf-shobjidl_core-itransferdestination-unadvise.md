---
UID: NF:shobjidl_core.ITransferDestination.Unadvise
title: ITransferDestination::Unadvise
author: windows-sdk-content
description: Terminates an advisory connection.
old-location: shell\ITransferDestination_Unadvise.htm
old-project: shell
ms.assetid: ecc3d32b-50cb-48d3-90c2-aba4614f863d
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ITransferDestination interface [Windows Shell],Unadvise method, ITransferDestination.Unadvise, ITransferDestination::Unadvise, Unadvise, Unadvise method [Windows Shell], Unadvise method [Windows Shell],ITransferDestination interface, _shell_ITransferDestination_Unadvise, shell.ITransferDestination_Unadvise, shobjidl_core/ITransferDestination::Unadvise
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ITransferDestination.Unadvise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ITransferDestination::Unadvise


## -description


Terminates an advisory connection.


## -parameters




### -param dwCookie [in]

Type: <b>DWORD</b>

A connection token previously returned from <a href="https://msdn.microsoft.com/e25040dd-bb51-45cc-99fb-9113e26d0baa">ITransferDestination::Advise</a>. Identifies the connection to be terminated.


## -returns



Type: <b>HRESULT</b>

Any HRESULTs other than those listed here indicate a failure.

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
The connection was successfully terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CONNECT_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>dwCookie</i> does not represent a valid connection.

</td>
</tr>
</table>
 




## -remarks



Terminates an advisory connection previously established through the <a href="https://msdn.microsoft.com/e25040dd-bb51-45cc-99fb-9113e26d0baa">ITransferDestination::Advise</a> method.



