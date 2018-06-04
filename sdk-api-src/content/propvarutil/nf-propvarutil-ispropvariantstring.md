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

# IsPropVariantString function


## -description


Specifies whether a specified <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure is a string type.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if <i>propvar</i> is a VT_LPWSTR or VT_BSTR <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>; otherwise, <b>FALSE</b>.




## -remarks



If this function returns <b>TRUE</b>, the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure referenced in <i>propvar</i> contains a Unicode string. To retrieve it, call <a href="shell.PropVariantToStringWithDefault">PropVariantToStringWithDefault</a> as shown here:

                

<code>PropVariantToStringWithDefault(propvar, NULL);</code>

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.



