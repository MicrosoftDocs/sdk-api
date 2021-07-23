---
UID: NF:shobjidl_core.IAssocHandler.GetName
title: IAssocHandler::GetName (shobjidl_core.h)
description: Retrieves the full path and file name of the executable file associated with the file type.
helpviewer_keywords: ["GetName","GetName method [Windows Shell]","GetName method [Windows Shell]","IAssocHandler interface","IAssocHandler interface [Windows Shell]","GetName method","IAssocHandler.GetName","IAssocHandler::GetName","_shell_IAssocHandler_GetName","shell.IAssocHandler_GetName","shobjidl_core/IAssocHandler::GetName"]
old-location: shell\IAssocHandler_GetName.htm
tech.root: shell
ms.assetid: d20aee32-fa5a-40a9-b0e2-8479a90fcf35
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Windows Shell], GetName method [Windows Shell],IAssocHandler interface, IAssocHandler interface [Windows Shell],GetName method, IAssocHandler.GetName, IAssocHandler::GetName, _shell_IAssocHandler_GetName, shell.IAssocHandler_GetName, shobjidl_core/IAssocHandler::GetName
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
 - IAssocHandler::GetName
 - shobjidl_core/IAssocHandler::GetName
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
 - IAssocHandler.GetName
---

# IAssocHandler::GetName


## -description

Retrieves the full path and file name of the executable file associated with the file type.

## -parameters

### -param ppsz [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated, Unicode string that contains the full path of the file, including the file name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler">IAssocHandler</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandler-getuiname">IAssocHandler::GetUIName</a>