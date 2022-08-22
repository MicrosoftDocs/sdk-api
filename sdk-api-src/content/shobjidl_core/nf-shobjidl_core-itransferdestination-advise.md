---
UID: NF:shobjidl_core.ITransferDestination.Advise
title: ITransferDestination::Advise (shobjidl_core.h)
description: Sets up an advisory connection for notifications on the status of file operations. (ITransferDestination.Advise)
helpviewer_keywords: ["Advise","Advise method [Windows Shell]","Advise method [Windows Shell]","ITransferDestination interface","ITransferDestination interface [Windows Shell]","Advise method","ITransferDestination.Advise","ITransferDestination::Advise","_shell_ITransferDestination_Advise","shell.ITransferDestination_Advise","shobjidl_core/ITransferDestination::Advise"]
old-location: shell\ITransferDestination_Advise.htm
tech.root: shell
ms.assetid: e25040dd-bb51-45cc-99fb-9113e26d0baa
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],ITransferDestination interface, ITransferDestination interface [Windows Shell],Advise method, ITransferDestination.Advise, ITransferDestination::Advise, _shell_ITransferDestination_Advise, shell.ITransferDestination_Advise, shobjidl_core/ITransferDestination::Advise
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITransferDestination::Advise
 - shobjidl_core/ITransferDestination::Advise
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ITransferDestination.Advise
---

# ITransferDestination::Advise


## -description

Sets up an advisory connection for notifications on the status of file operations.

## -parameters

### -param psink [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferadvisesink">ITransferAdviseSink</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferadvisesink">ITransferAdviseSink</a> notification interface to update the calling application using methods on this interface.

### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to a returned token that uniquely identifies this connection. The calling application uses this token later to delete the connection by passing it to the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferdestination-unadvise">ITransferDestination::Unadvise</a> method. If the connection is not successfully established, this value is zero.

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

Call <b>ITransferDestination::Advise</b> before calling any other <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination">ITransferDestination</a> methods so the handler can callback for any errors that might occur. If not set, the handler should consider it an indication that no feedback is available and do the "default" operation.
