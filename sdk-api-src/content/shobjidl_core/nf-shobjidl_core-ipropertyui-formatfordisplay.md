---
UID: NF:shobjidl_core.IPropertyUI.FormatForDisplay
title: IPropertyUI::FormatForDisplay (shobjidl_core.h)
description: Developers should use IPropertyDescription instead. Gets a formatted, Unicode string representation of a property value.
helpviewer_keywords: ["FormatForDisplay","FormatForDisplay method [Windows Properties]","FormatForDisplay method [Windows Properties]","IPropertyUI interface","IPropertyUI interface [Windows Properties]","FormatForDisplay method","IPropertyUI.FormatForDisplay","IPropertyUI::FormatForDisplay","PUIFFDF_DEFAULT","PUIFFDF_FRIENDLYDATE","PUIFFDF_NOTIME","PUIFFDF_RIGHTTOLEFT","PUIFFDF_SHORTFORMAT","_shell_IPropertyUI_FormatForDisplay","properties.IPropertyUI_FormatForDisplay","shell.IPropertyUI_FormatForDisplay","shobjidl_core/IPropertyUI::FormatForDisplay"]
old-location: properties\IPropertyUI_FormatForDisplay.htm
tech.root: properties
ms.assetid: 1283A5A9-EB9A-4e7c-A82B-0DDE309FA979
ms.date: 12/05/2018
ms.keywords: FormatForDisplay, FormatForDisplay method [Windows Properties], FormatForDisplay method [Windows Properties],IPropertyUI interface, IPropertyUI interface [Windows Properties],FormatForDisplay method, IPropertyUI.FormatForDisplay, IPropertyUI::FormatForDisplay, PUIFFDF_DEFAULT, PUIFFDF_FRIENDLYDATE, PUIFFDF_NOTIME, PUIFFDF_RIGHTTOLEFT, PUIFFDF_SHORTFORMAT, _shell_IPropertyUI_FormatForDisplay, properties.IPropertyUI_FormatForDisplay, shell.IPropertyUI_FormatForDisplay, shobjidl_core/IPropertyUI::FormatForDisplay
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
 - IPropertyUI::FormatForDisplay
 - shobjidl_core/IPropertyUI::FormatForDisplay
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
 - IPropertyUI.FormatForDisplay
---

# IPropertyUI::FormatForDisplay


## -description

Developers should use <a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a> instead. Gets a formatted, Unicode string representation of a property value.

## -parameters

### -param fmtid [in]

Type: <b>REFFMTID</b>

### -param pid [in]

Type: <b>PROPID</b>

### -param ppropvar [in]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

A <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that contains the type and value of the property.

### -param puiff [in]

Type: <b>PROPERTYUI_FORMAT_FLAGS</b>

The format for the returned property value.



#### PUIFFDF_DEFAULT (0x00000000)

0x00000000.



#### PUIFFDF_RIGHTTOLEFT (0x00000001)

0x00000001. Deprecated, do not use.



#### PUIFFDF_SHORTFORMAT (0x00000002)

0x00000002. Use the short format version of the string.



#### PUIFFDF_NOTIME (0x00000004)

0x00000004. Truncate time to days, not hours/mins/sec.



#### PUIFFDF_FRIENDLYDATE (0x00000008)

0x00000008. Use the friendly name for date: "Today", "Yesterday", and so on.

### -param pwszText [out]

Type: <b>LPWSTR</b>

The property value, formatted for display.

### -param cchText [in]

Type: <b>DWORD</b>

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.