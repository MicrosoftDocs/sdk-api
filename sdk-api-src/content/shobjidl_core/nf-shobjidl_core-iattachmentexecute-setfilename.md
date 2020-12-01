---
UID: NF:shobjidl_core.IAttachmentExecute.SetFileName
title: IAttachmentExecute::SetFileName (shobjidl_core.h)
description: Specifies and stores the proposed name of the file.
helpviewer_keywords: ["IAttachmentExecute interface [Windows Shell]","SetFileName method","IAttachmentExecute.SetFileName","IAttachmentExecute::SetFileName","SetFileName","SetFileName method [Windows Shell]","SetFileName method [Windows Shell]","IAttachmentExecute interface","_win32_IAttachmentExecute_SetFileName","shell.IAttachmentExecute_SetFileName","shobjidl_core/IAttachmentExecute::SetFileName"]
old-location: shell\IAttachmentExecute_SetFileName.htm
tech.root: shell
ms.assetid: 52dc823f-4429-4c1f-8906-9e4ee3f8158e
ms.date: 12/05/2018
ms.keywords: IAttachmentExecute interface [Windows Shell],SetFileName method, IAttachmentExecute.SetFileName, IAttachmentExecute::SetFileName, SetFileName, SetFileName method [Windows Shell], SetFileName method [Windows Shell],IAttachmentExecute interface, _win32_IAttachmentExecute_SetFileName, shell.IAttachmentExecute_SetFileName, shobjidl_core/IAttachmentExecute::SetFileName
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shdocvw.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAttachmentExecute::SetFileName
 - shobjidl_core/IAttachmentExecute::SetFileName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IAttachmentExecute.SetFileName
---

# IAttachmentExecute::SetFileName


## -description

Specifies and stores the proposed name of the file.

## -parameters

### -param pszFileName [in]

Type: <b>LPCWSTR</b>

A pointer to a string that contains the file name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code, including the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pszFileName</i> value is is set to <b>NULL</b>, points to an empty string, or points to a file name longer than <b>MAX_PATH</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The file name cannot be stored.

</td>
</tr>
</table>

## -remarks

No path information should be included at <i>pszFileName</i>, just the file's name.

<b>IAttachmentExecute::SetFileName</b> can be used by the calling application to check the validity of the file name before copying the file locally. The file name is checked for name collisions against other files stored at the local path location.

<b>IAttachmentExecute::SetFileName</b> is optional.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute">IAttachmentExecute</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setlocalpath">IAttachmentExecute::SetLocalPath</a>