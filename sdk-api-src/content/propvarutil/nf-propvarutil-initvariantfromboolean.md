---
UID: NF:propvarutil.InitVariantFromBoolean
title: InitVariantFromBoolean function (propvarutil.h)
author: windows-sdk-content
description: Initializes a VARIANT structure with a Boolean value.
old-location: properties\InitVariantFromBoolean.htm
tech.root: properties
ms.assetid: 155af0c9-bc1a-4d57-a2fc-dc22a0b1abe3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InitVariantFromBoolean, InitVariantFromBoolean function [Windows Properties], _shell_InitVariantFromBoolean, properties.InitVariantFromBoolean, propvarutil/InitVariantFromBoolean, shell.InitVariantFromBoolean
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
 - InitVariantFromBoolean
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitVariantFromBoolean function


## -description


Initializes a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure with a Boolean value.


## -parameters




### -param fVal [in]

Type: <b>BOOL</b>

Source <b>BOOL</b> value.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_BOOL variant.

Note that the <b>boolVal</b> structure member initialized by this function is of type <b>VARIANT_BOOL</b> and therefore can have values <b>VARIANT_TRUE</b> or <b>VARIANT_FALSE</b>. When you work with this structure member directly, use these constants instead of <b>TRUE</b> or <b>FALSE</b> because <b>VARIANT_TRUE</b> is not equal to <b>TRUE</b> and sizeof(VARIANT_TRUE) is not the same as sizeof(TRUE).

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762316(v=VS.85).aspx">InitVariantFromBoolean</a>.


```cpp
VARIANT var;

HRESULT hr = InitVariantFromBoolean(TRUE, &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_BOOL.
     VariantClear(&propvar);
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762287(v=VS.85).aspx">InitPropVariantFromBoolean</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776592(v=VS.85).aspx">VariantToBoolean</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776595(v=VS.85).aspx">VariantToBooleanWithDefault</a>
 

 

