---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IPropertyUI::GetDisplayName


## -description


Developers should use <a href="shell.IPropertyDescription">IPropertyDescription</a> instead. Gets a string specifying the name of the property suitable for display to users.


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



