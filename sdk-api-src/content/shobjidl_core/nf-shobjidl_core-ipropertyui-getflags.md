---
UID: NF:shobjidl_core.IPropertyUI.GetFlags
title: IPropertyUI::GetFlags (shobjidl_core.h)
description: Developers should use IPropertyDescription instead. Gets property feature flags for a specified property.
helpviewer_keywords: ["GetFlags","GetFlags method [Windows Properties]","GetFlags method [Windows Properties]","IPropertyUI interface","IPropertyUI interface [Windows Properties]","GetFlags method","IPropertyUI.GetFlags","IPropertyUI::GetFlags","_shell_IPropertyUI_GetFlags","properties.IPropertyUI_GetFlags","shell.IPropertyUI_GetFlags","shobjidl_core/IPropertyUI::GetFlags"]
old-location: properties\IPropertyUI_GetFlags.htm
tech.root: properties
ms.assetid: 8ADF50C1-CD6C-489c-9599-2AEB5C5FF00C
ms.date: 12/05/2018
ms.keywords: GetFlags, GetFlags method [Windows Properties], GetFlags method [Windows Properties],IPropertyUI interface, IPropertyUI interface [Windows Properties],GetFlags method, IPropertyUI.GetFlags, IPropertyUI::GetFlags, _shell_IPropertyUI_GetFlags, properties.IPropertyUI_GetFlags, shell.IPropertyUI_GetFlags, shobjidl_core/IPropertyUI::GetFlags
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IPropertyUI::GetFlags
 - shobjidl_core/IPropertyUI::GetFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPropertyUI.GetFlags
---

# IPropertyUI::GetFlags


## -description

Developers should use <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> instead. Gets property feature flags for a specified property.

## -parameters

### -param fmtid [in]

Type: <b>REFFMTID</b>

The FMTID of the property.

### -param pid [in]

Type: <b>PROPID</b>

The PROPID of the property.

### -param pflags [out]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_propertyui_flags">PROPERTYUI_FLAGS</a>*</b>

The <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_propertyui_flags">PROPERTYUI_FLAGS</a> for the property.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.