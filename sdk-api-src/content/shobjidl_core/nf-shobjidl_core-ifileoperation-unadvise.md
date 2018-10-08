---
UID: NF:shobjidl_core.IFileOperation.Unadvise
title: IFileOperation::Unadvise
author: windows-sdk-content
description: Terminates an advisory connection previously established through IFileOperation::Advise.
old-location: shell\IFileOperation_Unadvise.htm
tech.root: shell
ms.assetid: 684b3e94-50b9-465e-b4c3-b244fc7209f5
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IFileOperation interface [Windows Shell],Unadvise method, IFileOperation.Unadvise, IFileOperation::Unadvise, Unadvise, Unadvise method [Windows Shell], Unadvise method [Windows Shell],IFileOperation interface, _shell_IFileOperation_Unadvise, shell.IFileOperation_Unadvise, shobjidl_core/IFileOperation::Unadvise
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
 - IFileOperation.Unadvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOperation::Unadvise


## -description


Terminates an advisory connection previously established through <a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">IFileOperation::Advise</a>.


## -parameters




### -param dwCookie [in]

Type: <b>DWORD</b>

The connection token that identifies the connection to delete. This value was originally retrieved by <a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">Advise</a> when the connection was made.


## -returns



Type: <b>HRESULT</b>

Any value other than those listed here indicate a failure.

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
The connection was terminated successfully.

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
 




## -see-also




<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>



<a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">IFileOperation::Advise</a>
 

 

