---
UID: NF:shobjidl_core.IAttachmentExecute.ClearClientState
title: IAttachmentExecute::ClearClientState (shobjidl_core.h)
description: Removes any stored state that is based on the client's GUID. An example might be a setting based on a checked box that indicates a prompt should not be displayed again for a particular file type.
helpviewer_keywords: ["ClearClientState","ClearClientState method [Windows Shell]","ClearClientState method [Windows Shell]","IAttachmentExecute interface","IAttachmentExecute interface [Windows Shell]","ClearClientState method","IAttachmentExecute.ClearClientState","IAttachmentExecute::ClearClientState","shell.IAttachmentExecute_ClearClientState","shell_IAttachmentExecute_clearclientstate","shobjidl_core/IAttachmentExecute::ClearClientState"]
old-location: shell\IAttachmentExecute_ClearClientState.htm
tech.root: shell
ms.assetid: 238e78be-3306-4ac5-95a9-c7fa48c1c4fe
ms.date: 12/05/2018
ms.keywords: ClearClientState, ClearClientState method [Windows Shell], ClearClientState method [Windows Shell],IAttachmentExecute interface, IAttachmentExecute interface [Windows Shell],ClearClientState method, IAttachmentExecute.ClearClientState, IAttachmentExecute::ClearClientState, shell.IAttachmentExecute_ClearClientState, shell_IAttachmentExecute_clearclientstate, shobjidl_core/IAttachmentExecute::ClearClientState
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
 - IAttachmentExecute::ClearClientState
 - shobjidl_core/IAttachmentExecute::ClearClientState
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
 - IAttachmentExecute.ClearClientState
---

# IAttachmentExecute::ClearClientState


## -description

Removes any stored state that is based on the client's GUID. An example might be a setting based on a checked box that indicates a prompt should not be displayed again for a particular file type.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-setclientguid">IAttachmentExecute::SetClientGuid</a> must be called before using <b>IAttachmentExecute::ClearClientState</b>.
