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

# IPropertyUI::FormatForDisplay


## -description


Developers should use <a href="shell.IPropertyDescription">IPropertyDescription</a> instead. Gets a formatted, Unicode string representation of a property value.


## -parameters




### -param fmtid [in]

Type: <b>REFFMTID</b>


### -param pid [in]

Type: <b>PROPID</b>


### -param ppropvar [in]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

A <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains the type and value of the property.


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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



