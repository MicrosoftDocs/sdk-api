---
UID: NF:shobjidl_core.IAssocHandler.MakeDefault
title: IAssocHandler::MakeDefault (shobjidl_core.h)
description: Sets an application as the default application for this file type.
helpviewer_keywords: ["IAssocHandler interface [Windows Shell]","MakeDefault method","IAssocHandler.MakeDefault","IAssocHandler::MakeDefault","MakeDefault","MakeDefault method [Windows Shell]","MakeDefault method [Windows Shell]","IAssocHandler interface","_shell_IAssocHandler_MakeDefault","shell.IAssocHandler_MakeDefault","shobjidl_core/IAssocHandler::MakeDefault"]
old-location: shell\IAssocHandler_MakeDefault.htm
tech.root: shell
ms.assetid: 106ac493-bde6-4327-b3be-3132bfd47415
ms.date: 12/05/2018
ms.keywords: IAssocHandler interface [Windows Shell],MakeDefault method, IAssocHandler.MakeDefault, IAssocHandler::MakeDefault, MakeDefault, MakeDefault method [Windows Shell], MakeDefault method [Windows Shell],IAssocHandler interface, _shell_IAssocHandler_MakeDefault, shell.IAssocHandler_MakeDefault, shobjidl_core/IAssocHandler::MakeDefault
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
 - IAssocHandler::MakeDefault
 - shobjidl_core/IAssocHandler::MakeDefault
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
 - IAssocHandler.MakeDefault
---

# IAssocHandler::MakeDefault


## -description

Sets an application as the default application for this file type.

## -parameters

### -param pszDescription [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated, Unicode string that contains the display name of the application.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler">IAssocHandler</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-getuiname">IAssocHandler::GetUIName</a>