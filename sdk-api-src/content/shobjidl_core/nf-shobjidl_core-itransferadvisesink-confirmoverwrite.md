---
UID: NF:shobjidl_core.ITransferAdviseSink.ConfirmOverwrite
title: ITransferAdviseSink::ConfirmOverwrite (shobjidl_core.h)
description: Displays a message to the user confirming that overwriting existing items is acceptable.
helpviewer_keywords: ["ConfirmOverwrite","ConfirmOverwrite method [Windows Shell]","ConfirmOverwrite method [Windows Shell]","ITransferAdviseSink interface","ITransferAdviseSink interface [Windows Shell]","ConfirmOverwrite method","ITransferAdviseSink.ConfirmOverwrite","ITransferAdviseSink::ConfirmOverwrite","_shell_ITransferAdviseSink_ConfirmOverwrite","shell.ITransferAdviseSink_ConfirmOverwrite","shobjidl_core/ITransferAdviseSink::ConfirmOverwrite"]
old-location: shell\ITransferAdviseSink_ConfirmOverwrite.htm
tech.root: shell
ms.assetid: 1c7705c5-1a56-47c2-9b9b-3f72a4323cd7
ms.date: 12/05/2018
ms.keywords: ConfirmOverwrite, ConfirmOverwrite method [Windows Shell], ConfirmOverwrite method [Windows Shell],ITransferAdviseSink interface, ITransferAdviseSink interface [Windows Shell],ConfirmOverwrite method, ITransferAdviseSink.ConfirmOverwrite, ITransferAdviseSink::ConfirmOverwrite, _shell_ITransferAdviseSink_ConfirmOverwrite, shell.ITransferAdviseSink_ConfirmOverwrite, shobjidl_core/ITransferAdviseSink::ConfirmOverwrite
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
 - ITransferAdviseSink::ConfirmOverwrite
 - shobjidl_core/ITransferAdviseSink::ConfirmOverwrite
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
 - ITransferAdviseSink.ConfirmOverwrite
---

# ITransferAdviseSink::ConfirmOverwrite


## -description

Displays a message to the user confirming that overwriting existing items is acceptable.

## -parameters

### -param psiSource

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the source <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> .

### -param psiDestParent

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the destination parent folder <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

### -param pszName

Type: <b>LPCWSTR</b>

A pointer to a wide-string containing the desired name of the item at the destination. If <b>NULL</b>, the name is the same as the Shell item pointed to by <i>psiSource</i>.

## -returns

Type: <b>HRESULT</b>

The return values listed below are emitted specifically by this method to inform the calling process of how the operation ended.  If other results or errors are emitted during the operation of this method, they should be returned to the calling process.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_S_USER_IGNORED</b></dt>
</dl>
</td>
<td width="60%">
The user clicked <b>Ignore</b>. Allows the calling process to continue processing other files as appropriate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYENGINE_E_USER_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The user clicked <b>Cancel</b>. Stops processing of the current document and ends the current process.

</td>
</tr>
</table>