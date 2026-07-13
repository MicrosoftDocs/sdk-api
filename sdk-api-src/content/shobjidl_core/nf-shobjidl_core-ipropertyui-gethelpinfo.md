---
UID: NF:shobjidl_core.IPropertyUI.GetHelpInfo
title: IPropertyUI::GetHelpInfo (shobjidl_core.h)
description: Developers should use IPropertyDescription instead. (IPropertyUI.GetHelpInfo)
helpviewer_keywords: ["GetHelpInfo","GetHelpInfo method [Windows Properties]","GetHelpInfo method [Windows Properties]","IPropertyUI interface","IPropertyUI interface [Windows Properties]","GetHelpInfo method","IPropertyUI.GetHelpInfo","IPropertyUI::GetHelpInfo","_shell_IPropertyUI_GetHelpInfo","properties.IPropertyUI_GetHelpInfo","shell.IPropertyUI_GetHelpInfo","shobjidl_core/IPropertyUI::GetHelpInfo"]
old-location: properties\IPropertyUI_GetHelpInfo.htm
tech.root: properties
ms.assetid: 165ABA55-7CDB-48cf-AE14-DA314197BA42
ms.date: 12/05/2018
ms.keywords: GetHelpInfo, GetHelpInfo method [Windows Properties], GetHelpInfo method [Windows Properties],IPropertyUI interface, IPropertyUI interface [Windows Properties],GetHelpInfo method, IPropertyUI.GetHelpInfo, IPropertyUI::GetHelpInfo, _shell_IPropertyUI_GetHelpInfo, properties.IPropertyUI_GetHelpInfo, shell.IPropertyUI_GetHelpInfo, shobjidl_core/IPropertyUI::GetHelpInfo
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
 - IPropertyUI::GetHelpInfo
 - shobjidl_core/IPropertyUI::GetHelpInfo
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
 - IPropertyUI.GetHelpInfo
---

# IPropertyUI::GetHelpInfo


## -description

Developers should use <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> instead. Gets

## -parameters

### -param fmtid [in]

Type: <b>REFFMTID</b>

The FMTID of the property.

### -param pid [in]

Type: <b>PROPID</b>

The PROPID of the property.

### -param pwszHelpFile [out]

Type: <b>LPWSTR</b>

The fully qualified path of the Help file.

### -param cch [in]

Type: <b>DWORD</b>

### -param puHelpID [out]

Type: <b>UINT*</b>

The Help context ID for the property.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
