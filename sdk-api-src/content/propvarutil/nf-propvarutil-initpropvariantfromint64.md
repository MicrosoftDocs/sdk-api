---
UID: NF:propvarutil.InitPropVariantFromInt64
title: InitPropVariantFromInt64 function (propvarutil.h)
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a specified Int64 value.
old-location: properties\InitPropVariantFromInt64.htm
tech.root: properties
ms.assetid: 2a2a5348-4d3d-475c-8039-097b4dacf7cb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromInt64, InitPropVariantFromInt64 function [Windows Properties], properties.InitPropVariantFromInt64, propvarutil/InitPropVariantFromInt64, shell.InitPropVariantFromInt64, shell_InitPropVariantFromInt64
ms.topic: function
f1_keywords: 
 - "propvarutil/InitPropVariantFromInt64"
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
 - InitPropVariantFromInt64
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# InitPropVariantFromInt64 function


## -description


Initializes a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a specified <b>Int64</b> value.


## -parameters




### -param llVal [in]

Type: <b>LONGLONG</b>

The source <b>LONGLONG</b> value.


### -param ppropvar [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_I8 propvariant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromint64">InitPropVariantFromInt64</a>.


```cpp
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromInt64(4096, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_I8.
 
    PropVariantClear(&propvar);
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromint64">InitVariantFromInt64</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint64">PropVariantToInt64</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttoint64withdefault">PropVariantToInt64WithDefault</a>
 

 

