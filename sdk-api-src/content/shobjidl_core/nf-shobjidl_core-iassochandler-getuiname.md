---
UID: NF:shobjidl_core.IAssocHandler.GetUIName
title: IAssocHandler::GetUIName (shobjidl_core.h)
description: Retrieves the display name of an application.
helpviewer_keywords: ["GetUIName","GetUIName method [Windows Shell]","GetUIName method [Windows Shell]","IAssocHandler interface","IAssocHandler interface [Windows Shell]","GetUIName method","IAssocHandler.GetUIName","IAssocHandler::GetUIName","_shell_IAssocHandler_GetUIName","shell.IAssocHandler_GetUIName","shobjidl_core/IAssocHandler::GetUIName"]
old-location: shell\IAssocHandler_GetUIName.htm
tech.root: shell
ms.assetid: bf714cf9-a16a-40a4-8dd8-c53c289967f5
ms.date: 12/05/2018
ms.keywords: GetUIName, GetUIName method [Windows Shell], GetUIName method [Windows Shell],IAssocHandler interface, IAssocHandler interface [Windows Shell],GetUIName method, IAssocHandler.GetUIName, IAssocHandler::GetUIName, _shell_IAssocHandler_GetUIName, shell.IAssocHandler_GetUIName, shobjidl_core/IAssocHandler::GetUIName
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
 - IAssocHandler::GetUIName
 - shobjidl_core/IAssocHandler::GetUIName
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
 - IAssocHandler.GetUIName
---

# IAssocHandler::GetUIName


## -description

Retrieves the display name of an application.

## -parameters

### -param ppsz [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated, Unicode string that contains the display name of the application.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler">IAssocHandler</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-getname">IAssocHandler::GetName</a>