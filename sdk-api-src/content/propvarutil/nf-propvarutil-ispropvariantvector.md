---
UID: NF:propvarutil.IsPropVariantVector
title: IsPropVariantVector function
author: windows-sdk-content
description: Specifies whether a PROPVARIANT structure has a vector type.
old-location: properties\IsPropVariantVector.htm
old-project: properties
ms.assetid: c094c636-e51d-4a61-8d92-90abe2f0446e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IsPropVariantVector, IsPropVariantVector function [Windows Properties], properties.IsPropVariantVector, propvarutil/IsPropVariantVector, shell.IsPropVariantVector, shell_IsPropVariantVector
ms.prod: windows
ms.technology: windows-sdk
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
-	IsPropVariantVector
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IsPropVariantVector function


## -description


Specifies whether a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure has a vector type.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure being queried.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if <i>propvar</i> is a VT_ARRAY | VT_VECTOR <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>; otherwise, <b>FALSE</b>.




## -remarks



This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.



