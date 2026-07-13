---
UID: NF:shobjidl_core.IShellItem2.GetPropertyDescriptionList
title: IShellItem2::GetPropertyDescriptionList (shobjidl_core.h)
description: Gets a property description list object given a reference to a property key.
helpviewer_keywords: ["GetPropertyDescriptionList","GetPropertyDescriptionList method [Windows Shell]","GetPropertyDescriptionList method [Windows Shell]","IShellItem2 interface","IShellItem2 interface [Windows Shell]","GetPropertyDescriptionList method","IShellItem2.GetPropertyDescriptionList","IShellItem2::GetPropertyDescriptionList","_shell_IShellItem2_GetPropertyDescriptionList","shell.IShellItem2_GetPropertyDescriptionList","shobjidl_core/IShellItem2::GetPropertyDescriptionList"]
old-location: shell\IShellItem2_GetPropertyDescriptionList.htm
tech.root: shell
ms.assetid: 443b95c9-0a9e-4ad5-8774-ad3b1b51c136
ms.date: 12/05/2018
ms.keywords: GetPropertyDescriptionList, GetPropertyDescriptionList method [Windows Shell], GetPropertyDescriptionList method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetPropertyDescriptionList method, IShellItem2.GetPropertyDescriptionList, IShellItem2::GetPropertyDescriptionList, _shell_IShellItem2_GetPropertyDescriptionList, shell.IShellItem2_GetPropertyDescriptionList, shobjidl_core/IShellItem2::GetPropertyDescriptionList
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
 - IShellItem2::GetPropertyDescriptionList
 - shobjidl_core/IShellItem2::GetPropertyDescriptionList
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
 - IShellItem2.GetPropertyDescriptionList
---

# IShellItem2::GetPropertyDescriptionList


## -description

Gets a property description list object given a reference to a property key.

## -parameters

### -param keyType [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param riid [in]

Type: <b>REFIID</b>

A reference to a desired IID.

### -param ppv [out]

Type: <b>void**</b>

Contains the address of an <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionlist">IPropertyDescriptionList</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.