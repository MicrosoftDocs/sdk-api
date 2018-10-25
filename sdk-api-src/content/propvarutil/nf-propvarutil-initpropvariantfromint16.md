---
UID: NF:propvarutil.InitPropVariantFromInt16
title: InitPropVariantFromInt16 function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a 16-bit integer value.
old-location: properties\InitPropVariantFromInt16.htm
tech.root: properties
ms.assetid: fb58c71c-f6ff-408e-9375-98654a41cf11
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: InitPropVariantFromInt16, InitPropVariantFromInt16 function [Windows Properties], properties.InitPropVariantFromInt16, propvarutil/InitPropVariantFromInt16, shell.InitPropVariantFromInt16, shell_InitPropVariantFromInt16
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propvarutil.h
api_name:
 - InitPropVariantFromInt16
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitPropVariantFromInt16 function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a 16-bit integer value.


## -parameters




### -param nVal [in]

Type: <b>SHORT</b>

The source <b>SHORT</b> value.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function creates a VT_I2 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantFromInt16">InitPropVariantFromInt16</a>.


```cpp
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromInt16(42, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_I2.
 
    PropVariantClear(&propvar);
}
```





## -see-also




<a href="shell.InitPropVariantFromInt16Vector">InitPropVariantFromInt16Vector</a>



<a href="shell.InitVariantFromInt16">InitVariantFromInt16</a>



<a href="shell.PropVariantToInt16">PropVariantToInt16</a>



<a href="shell.PropVariantToInt16WithDefault">PropVariantToInt16WithDefault</a>
 

 

