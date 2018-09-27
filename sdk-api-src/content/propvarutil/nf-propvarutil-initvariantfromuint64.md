---
UID: NF:propvarutil.InitVariantFromUInt64
title: InitVariantFromUInt64 function
author: windows-sdk-content
description: Initializes a VARIANT structure with an unsigned 64-bit integer value.
old-location: properties\InitVariantFromUInt64.htm
tech.root: properties
ms.assetid: 8fa8bfe9-b9a6-4292-b303-621ef9d8aa4d
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: InitVariantFromUInt64, InitVariantFromUInt64 function [Windows Properties], _shell_InitVariantFromUInt64, properties.InitVariantFromUInt64, propvarutil/InitVariantFromUInt64, shell.InitVariantFromUInt64
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
 - InitVariantFromUInt64
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitVariantFromUInt64 function


## -description


Initializes a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure with an unsigned 64-bit integer value.


## -parameters




### -param ullVal [in]

Type: <b>ULONGLONG</b>

Source <b>ULONGLONG</b> value.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_UI8 variant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitVariantFromUInt64">InitVariantFromUInt64</a>.


```cpp
VARIANT var;

HRESULT hr = InitVariantFromUInt64(3176, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_UI8.
    VariantClear(&propvar);
}
```





## -see-also




<a href="shell.InitPropVariantFromUInt64">InitPropVariantFromUInt64</a>



<a href="shell.VariantToUInt64">VariantToUInt64</a>



<a href="shell.VariantToUInt64WithDefault">VariantToUInt64WithDefault</a>
 

 

