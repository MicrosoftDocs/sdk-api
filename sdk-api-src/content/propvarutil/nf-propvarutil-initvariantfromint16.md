---
UID: NF:propvarutil.InitVariantFromInt16
title: InitVariantFromInt16 function
author: windows-sdk-content
description: Initializes a VARIANT structure with a 16-bit integer value.
old-location: properties\InitVariantFromInt16.htm
tech.root: properties
ms.assetid: 8ccb09bf-a2d2-4637-b8b1-e7abe83b846d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InitVariantFromInt16, InitVariantFromInt16 function [Windows Properties], _shell_InitVariantFromInt16, properties.InitVariantFromInt16, propvarutil/InitVariantFromInt16, shell.InitVariantFromInt16
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
 - InitVariantFromInt16
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitVariantFromInt16 function


## -description


Initializes a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure with a 16-bit integer value.


## -parameters




### -param iVal [in]

Type: <b>SHORT</b>

Source <b>SHORT</b> value.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_I2 variant.

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762327(v=VS.85).aspx">InitVariantFromInt16</a>.


```cpp
VARIANT var;

HRESULT hr = InitVariantFromInt16(3, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_I2.
    VariantClear(&propvar);
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762297(v=VS.85).aspx">InitPropVariantFromInt16</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776604(v=VS.85).aspx">VariantToInt16</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776607(v=VS.85).aspx">VariantToInt16WithDefault</a>
 

 

