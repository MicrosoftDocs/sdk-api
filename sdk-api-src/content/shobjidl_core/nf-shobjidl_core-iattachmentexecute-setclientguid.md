---
UID: NF:shobjidl_core.IAttachmentExecute.SetClientGuid
title: IAttachmentExecute::SetClientGuid (shobjidl_core.h)
description: Specifies and stores the GUID for the client.
helpviewer_keywords: ["IAttachmentExecute interface [Windows Shell]","SetClientGuid method","IAttachmentExecute.SetClientGuid","IAttachmentExecute::SetClientGuid","SetClientGuid","SetClientGuid method [Windows Shell]","SetClientGuid method [Windows Shell]","IAttachmentExecute interface","_win32_IAttachmentExecute_SetClientGuid","shell.IAttachmentExecute_SetClientGuid","shobjidl_core/IAttachmentExecute::SetClientGuid"]
old-location: shell\IAttachmentExecute_SetClientGuid.htm
tech.root: shell
ms.assetid: d0ee35f7-c23e-450b-8b90-0fb5744263fd
ms.date: 12/05/2018
ms.keywords: IAttachmentExecute interface [Windows Shell],SetClientGuid method, IAttachmentExecute.SetClientGuid, IAttachmentExecute::SetClientGuid, SetClientGuid, SetClientGuid method [Windows Shell], SetClientGuid method [Windows Shell],IAttachmentExecute interface, _win32_IAttachmentExecute_SetClientGuid, shell.IAttachmentExecute_SetClientGuid, shobjidl_core/IAttachmentExecute::SetClientGuid
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
 - IAttachmentExecute::SetClientGuid
 - shobjidl_core/IAttachmentExecute::SetClientGuid
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
 - IAttachmentExecute.SetClientGuid
---

# IAttachmentExecute::SetClientGuid


## -description

Specifies and stores the GUID for the client.

## -parameters

### -param guid [in]

Type: <b>REFGUID</b>

The GUID that represents the client.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A user can choose not to display certain prompts. That information is stored in the registry on a per-client basis, indexed by <i>guid</i>.

