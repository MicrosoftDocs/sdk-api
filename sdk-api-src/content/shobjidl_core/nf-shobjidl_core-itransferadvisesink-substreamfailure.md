---
UID: NF:shobjidl_core.ITransferAdviseSink.SubStreamFailure
title: ITransferAdviseSink::SubStreamFailure (shobjidl_core.h)
description: Called when there is a failure that involves secondary streams and user interaction is needed.
helpviewer_keywords: ["ITransferAdviseSink interface [Windows Shell]","SubStreamFailure method","ITransferAdviseSink.SubStreamFailure","ITransferAdviseSink::SubStreamFailure","SubStreamFailure","SubStreamFailure method [Windows Shell]","SubStreamFailure method [Windows Shell]","ITransferAdviseSink interface","_shell_ITransferAdviseSink_SubStreamFailure","shell.ITransferAdviseSink_SubStreamFailure","shobjidl_core/ITransferAdviseSink::SubStreamFailure"]
old-location: shell\ITransferAdviseSink_SubStreamFailure.htm
tech.root: shell
ms.assetid: 4cca3bc0-45c6-40ee-8050-7035faa1e601
ms.date: 12/05/2018
ms.keywords: ITransferAdviseSink interface [Windows Shell],SubStreamFailure method, ITransferAdviseSink.SubStreamFailure, ITransferAdviseSink::SubStreamFailure, SubStreamFailure, SubStreamFailure method [Windows Shell], SubStreamFailure method [Windows Shell],ITransferAdviseSink interface, _shell_ITransferAdviseSink_SubStreamFailure, shell.ITransferAdviseSink_SubStreamFailure, shobjidl_core/ITransferAdviseSink::SubStreamFailure
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
 - ITransferAdviseSink::SubStreamFailure
 - shobjidl_core/ITransferAdviseSink::SubStreamFailure
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
 - ITransferAdviseSink.SubStreamFailure
---

# ITransferAdviseSink::SubStreamFailure


## -description

Called when there is a failure that involves secondary streams and user interaction is needed.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that caused the failure.

### -param pszStreamName [in]

Type: <b>LPCWSTR</b>

The name of the data that will be lost in the operation.

### -param hrError [in]

Type: <b>HRESULT</b>

The error code that was generated. It must be handled by the copy engine.

## -returns

Type: <b>HRESULT</b>

Any other <b>HRESULT</b> should be passed up. If the failure is not handled, the return value should be <i>hrError</i>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_USERRETRY</b></dt>
</dl>
</td>
<td width="60%">
The handler should retry the file operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_USERRETRYWITHNEWNAME</b></dt>
</dl>
</td>
<td width="60%">
The handler should retry the file operation using the name returned in the <i>pszRename</i> buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_OVERWRITE</b></dt>
</dl>
</td>
<td width="60%">
The user has indicated that the handler should overwrite the existing file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_RETRYWITHOUTSECURITY</b></dt>
</dl>
</td>
<td width="60%">
The user has indicated that the handler should try the operation again without the security descriptor.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_E_USERCANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The user clicked <b>Cancel</b>. The entire copy job is being terminated. The handler should return this code back to the copy engine.

</td>
</tr>
</table>