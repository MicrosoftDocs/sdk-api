---
UID: NF:shobjidl_core.ITransferSource.Advise
title: ITransferSource::Advise (shobjidl_core.h)
description: Sets up an advisory connection for notifications on the status of file operations. (ITransferSource.Advise)
helpviewer_keywords: ["Advise","Advise method [Windows Shell]","Advise method [Windows Shell]","ITransferSource interface","ITransferSource interface [Windows Shell]","Advise method","ITransferSource.Advise","ITransferSource::Advise","_shell_ITransferSource_Advise","shell.ITransferSource_Advise","shobjidl_core/ITransferSource::Advise"]
old-location: shell\ITransferSource_Advise.htm
tech.root: shell
ms.assetid: 5a546603-d409-4c8e-9fa8-892c5c4844e7
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [Windows Shell], Advise method [Windows Shell],ITransferSource interface, ITransferSource interface [Windows Shell],Advise method, ITransferSource.Advise, ITransferSource::Advise, _shell_ITransferSource_Advise, shell.ITransferSource_Advise, shobjidl_core/ITransferSource::Advise
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
 - ITransferSource::Advise
 - shobjidl_core/ITransferSource::Advise
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
 - ITransferSource.Advise
---

# ITransferSource::Advise


## -description

Sets up an advisory connection for notifications on the status of file operations.

## -parameters

### -param psink [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferadvisesink">ITransferAdviseSink</a>*</b>

A pointer to notification interface <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferadvisesink">ITransferAdviseSink</a> to update the calling application using methods on this interface.

### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to a returned token that uniquely identifies this connection. The calling application uses this token later to delete the connection by passing it to the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-unadvise">ITransferSource::Unadvise</a> method. If the connection was not successfully established, this value is zero.

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

Call <b>ITransferSource::Advise</b> before calling any other methods in this interface to enable an advisory session. If not set, the handler should consider it an indication that no feedback is available and to do the "default" operation without consulting the calling application.
