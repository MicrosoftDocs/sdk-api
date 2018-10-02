---
UID: NF:propvarutil.InitPropVariantFromStringVector
title: InitPropVariantFromStringVector function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure from a specified string vector.
old-location: properties\InitPropVariantFromStringVector.htm
tech.root: properties
ms.assetid: 4190337f-f9f6-4584-b667-6b96c1ce48c8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: InitPropVariantFromStringVector, InitPropVariantFromStringVector function [Windows Properties], properties.InitPropVariantFromStringVector, propvarutil/InitPropVariantFromStringVector, shell.InitPropVariantFromStringVector, shell_InitPropVariantFromStringVector
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
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - InitPropVariantFromStringVector
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitPropVariantFromStringVector function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure from a specified string vector.


## -parameters




### -param prgsz [in]

Type: <b>PCWSTR*</b>

Pointer to a buffer that contains the source string vector.


### -param cElems [in]

Type: <b>ULONG</b>

The number of vector elements in <i>prgsz</i>.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="shell.InitPropVariantFromString">InitPropVariantFromString</a>



<a href="shell.InitPropVariantFromStringAsVector">InitPropVariantFromStringAsVector</a>



<a href="shell.InitVariantFromString">InitVariantFromString</a>



<a href="shell.PropVariantToStringVector">PropVariantToStringVector</a>
 

 

