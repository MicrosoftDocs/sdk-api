---
UID: NF:shobjidl_core.IObjectWithProgID.SetProgID
title: IObjectWithProgID::SetProgID (shobjidl_core.h)
description: Sets the ProgID of an object.
helpviewer_keywords: ["IObjectWithProgID interface [Windows Shell]","SetProgID method","IObjectWithProgID.SetProgID","IObjectWithProgID::SetProgID","SetProgID","SetProgID method [Windows Shell]","SetProgID method [Windows Shell]","IObjectWithProgID interface","_shell_IObjectWithProgID_SetProgID","shell.IObjectWithProgID_SetProgID","shobjidl_core/IObjectWithProgID::SetProgID"]
old-location: shell\IObjectWithProgID_SetProgID.htm
tech.root: shell
ms.assetid: 4889f9a5-da80-4909-b4b5-4ea69ea99c3e
ms.date: 12/05/2018
ms.keywords: IObjectWithProgID interface [Windows Shell],SetProgID method, IObjectWithProgID.SetProgID, IObjectWithProgID::SetProgID, SetProgID, SetProgID method [Windows Shell], SetProgID method [Windows Shell],IObjectWithProgID interface, _shell_IObjectWithProgID_SetProgID, shell.IObjectWithProgID_SetProgID, shobjidl_core/IObjectWithProgID::SetProgID
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IObjectWithProgID::SetProgID
 - shobjidl_core/IObjectWithProgID::SetProgID
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
 - IObjectWithProgID.SetProgID
---

# IObjectWithProgID::SetProgID


## -description

Sets the ProgID of an object.

## -parameters

### -param pszProgID [in]

Type: <b>LPCWSTR</b>

A pointer to a string that contains the new ProgID.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithprogid">IObjectWithProgID</a>



<a href="/windows/desktop/shell/fa-progids">Programmatic Identifiers</a>