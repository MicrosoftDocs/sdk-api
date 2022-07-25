---
UID: NF:shobjidl_core.IPropertyUI.GetDefaultWidth
title: IPropertyUI::GetDefaultWidth (shobjidl_core.h)
description: Developers should use IPropertyDescription instead. Gets the width of the property description.
helpviewer_keywords: ["GetDefaultWidth","GetDefaultWidth method [Windows Properties]","GetDefaultWidth method [Windows Properties]","IPropertyUI interface","IPropertyUI interface [Windows Properties]","GetDefaultWidth method","IPropertyUI.GetDefaultWidth","IPropertyUI::GetDefaultWidth","_shell_IPropertyUI_GetDefaultWidth","properties.IPropertyUI_GetDefaultWidth","shell.IPropertyUI_GetDefaultWidth","shobjidl_core/IPropertyUI::GetDefaultWidth"]
old-location: properties\IPropertyUI_GetDefaultWidth.htm
tech.root: properties
ms.assetid: 51A283CF-FA15-478c-B93B-75347308AEEB
ms.date: 12/05/2018
ms.keywords: GetDefaultWidth, GetDefaultWidth method [Windows Properties], GetDefaultWidth method [Windows Properties],IPropertyUI interface, IPropertyUI interface [Windows Properties],GetDefaultWidth method, IPropertyUI.GetDefaultWidth, IPropertyUI::GetDefaultWidth, _shell_IPropertyUI_GetDefaultWidth, properties.IPropertyUI_GetDefaultWidth, shell.IPropertyUI_GetDefaultWidth, shobjidl_core/IPropertyUI::GetDefaultWidth
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
 - IPropertyUI::GetDefaultWidth
 - shobjidl_core/IPropertyUI::GetDefaultWidth
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
 - IPropertyUI.GetDefaultWidth
---

# IPropertyUI::GetDefaultWidth


## -description

Developers should use <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> instead. Gets the width of the property description.

## -parameters

### -param fmtid [in]

Type: <b>REFFMTID</b>

The FMTID of the property.

### -param pid [in]

Type: <b>PROPID</b>

The PROPID of the property.

### -param pcxChars [out]

Type: <b>ULONG*</b>

The width of the property description.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.