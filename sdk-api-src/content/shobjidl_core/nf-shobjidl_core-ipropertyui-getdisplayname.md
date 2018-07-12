---
UID: NF:shobjidl_core.IPropertyUI.GetDisplayName
title: IPropertyUI::GetDisplayName
author: windows-sdk-content
description: Developers should use IPropertyDescription instead. Gets a string specifying the name of the property suitable for display to users.
old-location: properties\IPropertyUI_GetDisaplayName.htm
old-project: properties
ms.assetid: F1B97A0C-B21F-45d6-8B2D-02BFF74C9CEE
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetDisplayName, GetDisplayName method [Windows Properties], GetDisplayName method [Windows Properties],IPropertyUI interface, IPropertyUI interface [Windows Properties],GetDisplayName method, IPropertyUI.GetDisplayName, IPropertyUI::GetDisplayName, PUIFNF_DEFAULT, PUIFNF_MNEMONIC, _shell_IPropertyUI_GetDisaplayName, properties.IPropertyUI_GetDisaplayName, shell.IPropertyUI_GetDisaplayName, shobjidl_core/IPropertyUI::GetDisplayName
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPropertyUI.GetDisplayName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IPropertyUI::GetDisplayName


## -description


Developers should use <a href="https://msdn.microsoft.com/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a> instead. Gets a string specifying the name of the property suitable for display to users.


## -parameters




### -param fmtid [in]

Type: <b>REFFMTID</b>

The FMTID of the property.


### -param pid [in]

Type: <b>PROPID</b>

The PROPID of the property.


### -param flags [in]

Type: <b>PROPERTYUI_NAME_FLAGS</b>

One of the following PROPERTYUI_NAME_FLAGS values:



#### PUIFNF_DEFAULT (0x00000000)

0x00000000.



#### PUIFNF_MNEMONIC (0x00000001)

0x00000001. Include mnemonic in display name.


### -param pwszText [out]

Type: <b>LPWSTR</b>

A string specifying the property.


### -param cchText [in]

Type: <b>DWORD</b>

The length of the property display name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



