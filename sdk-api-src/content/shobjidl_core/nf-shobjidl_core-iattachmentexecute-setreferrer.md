---
UID: NF:shobjidl_core.IAttachmentExecute.SetReferrer
title: IAttachmentExecute::SetReferrer (shobjidl_core.h)
description: Sets the security zone associated with the attachment file based on the referring file.
helpviewer_keywords: ["IAttachmentExecute interface [Windows Shell]","SetReferrer method","IAttachmentExecute.SetReferrer","IAttachmentExecute::SetReferrer","SetReferrer","SetReferrer method [Windows Shell]","SetReferrer method [Windows Shell]","IAttachmentExecute interface","_win32_IAttachmentExecute_SetReferrer","shell.IAttachmentExecute_SetReferrer","shobjidl_core/IAttachmentExecute::SetReferrer"]
old-location: shell\IAttachmentExecute_SetReferrer.htm
tech.root: shell
ms.assetid: d7ee869a-2afe-4d98-a0bb-d80e57425079
ms.date: 12/05/2018
ms.keywords: IAttachmentExecute interface [Windows Shell],SetReferrer method, IAttachmentExecute.SetReferrer, IAttachmentExecute::SetReferrer, SetReferrer, SetReferrer method [Windows Shell], SetReferrer method [Windows Shell],IAttachmentExecute interface, _win32_IAttachmentExecute_SetReferrer, shell.IAttachmentExecute_SetReferrer, shobjidl_core/IAttachmentExecute::SetReferrer
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
 - IAttachmentExecute::SetReferrer
 - shobjidl_core/IAttachmentExecute::SetReferrer
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
 - IAttachmentExecute.SetReferrer
---

# IAttachmentExecute::SetReferrer


## -description

Sets the security zone associated with the attachment file based on the referring file.

## -parameters

### -param pszReferrer [in]

Type: <b>LPCWSTR</b>

A pointer to a string containing the path of the referring file.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IAttachmentExecute::SetReferrer</b> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setsource">IAttachmentExecute::SetSource</a> have similar functionality. If both are set, the least-trusted zone of the two is used.

<b>IAttachmentExecute::SetReferrer</b> is used by container files to indicate indirect inheritance and avoid zone elevation. It can also be used with shortcut files to limit elevation based on parameters.

Calling <b>IAttachmentExecute::SetReferrer</b> is optional.

<b>IAttachmentExecute::SetReferrer</b> is only used to determine the security zone and its associated policies.