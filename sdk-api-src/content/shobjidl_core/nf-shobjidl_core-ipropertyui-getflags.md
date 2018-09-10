---
UID: NF:shobjidl_core.IPropertyUI.GetFlags
title: IPropertyUI::GetFlags
author: windows-sdk-content
description: Developers should use IPropertyDescription instead. Gets property feature flags for a specified property.
old-location: properties\IPropertyUI_GetFlags.htm
tech.root: properties
ms.assetid: 8ADF50C1-CD6C-489c-9599-2AEB5C5FF00C
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetFlags, GetFlags method [Windows Properties], GetFlags method [Windows Properties],IPropertyUI interface, IPropertyUI interface [Windows Properties],GetFlags method, IPropertyUI.GetFlags, IPropertyUI::GetFlags, _shell_IPropertyUI_GetFlags, properties.IPropertyUI_GetFlags, shell.IPropertyUI_GetFlags, shobjidl_core/IPropertyUI::GetFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPropertyUI.GetFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyUI::GetFlags


## -description


Developers should use <a href="shell.IPropertyDescription">IPropertyDescription</a> instead. Gets property feature flags for a specified property.


## -parameters




### -param fmtid [in]

Type: <b>REFFMTID</b>

The FMTID of the property.


### -param pid [in]

Type: <b>PROPID</b>

The PROPID of the property.


### -param pflags [out]

Type: <b><a href="shell.PROPERTYUI_FLAGS">PROPERTYUI_FLAGS</a>*</b>

The <a href="shell.PROPERTYUI_FLAGS">PROPERTYUI_FLAGS</a> for the property.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



