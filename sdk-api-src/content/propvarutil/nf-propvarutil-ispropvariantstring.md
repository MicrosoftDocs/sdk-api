---
UID: NF:propvarutil.IsPropVariantString
title: IsPropVariantString function
author: windows-driver-content
description: Specifies whether a specified PROPVARIANT structure is a string type.
old-location: properties\IsPropVariantString.htm
old-project: properties
ms.assetid: 3f580098-6bfb-41bd-b43d-986ee00b9c75
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IsPropVariantString, IsPropVariantString function [Windows Properties], properties.IsPropVariantString, propvarutil/IsPropVariantString, shell.IsPropVariantString, shell_IsPropVariantString
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Propvarutil.h
api_name:
-	IsPropVariantString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
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



