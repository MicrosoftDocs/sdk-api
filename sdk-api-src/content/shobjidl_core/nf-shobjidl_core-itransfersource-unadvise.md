---
UID: NF:shobjidl_core.ITransferSource.Unadvise
title: ITransferSource::Unadvise
author: windows-sdk-content
description: Terminates an advisory connection.
old-location: shell\ITransferSource_Unadvise.htm
tech.root: shell
ms.assetid: 4f71134e-dfbf-40e7-b72b-c4913c876689
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ITransferSource interface [Windows Shell],Unadvise method, ITransferSource.Unadvise, ITransferSource::Unadvise, Unadvise, Unadvise method [Windows Shell], Unadvise method [Windows Shell],ITransferSource interface, _shell_ITransferSource_Unadvise, shell.ITransferSource_Unadvise, shobjidl_core/ITransferSource::Unadvise
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
 - ITransferSource.Unadvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransferSource::Unadvise


## -description


Terminates an advisory connection.


## -parameters




### -param dwCookie [in]

Type: <b>DWORD</b>

The connection token previously returned from method <a href="https://msdn.microsoft.com/5a546603-d409-4c8e-9fa8-892c5c4844e7">ITransferSource::Advise</a>.


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
The value in dwCookie does not represent a valid connection.

</td>
</tr>
</table>
 




## -remarks



Terminates an advisory connection previously established through  method <a href="https://msdn.microsoft.com/5a546603-d409-4c8e-9fa8-892c5c4844e7">ITransferSource::Advise</a>. The <i>dwCookie</i> parameter identifies the connection to terminate.



