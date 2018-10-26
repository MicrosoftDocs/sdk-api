---
UID: NF:propvarutil.VariantToDouble
title: VariantToDouble function
author: windows-sdk-content
description: Extracts a DOUBLE value from a VARIANT structure. If no value can be extracted, then a default value is assigned.
old-location: properties\VariantToDouble.htm
tech.root: properties
ms.assetid: 7bd756c6-f02a-4cf4-9458-b3304e2da2db
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: VariantToDouble, VariantToDouble function [Windows Properties], _shell_VariantToDouble, properties.VariantToDouble, propvarutil/VariantToDouble, shell.VariantToDouble
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
 - VariantToDouble
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# VariantToDouble function


## -description


Extracts a <b>DOUBLE</b> value from a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure. If no value can be extracted, then a default value is assigned.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure.


### -param pdblRet [out]

Type: <b>DOUBLE*</b>

When this function returns, contains the extracted value if one exists; otherwise, 0.0.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used when the calling application expects a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> to hold a <b>DOUBLE</b> value. For instance, an application that obtains values from a Shell folder can use this function to safely extract the value from one of the folder's properties whose value is stored as a <b>DOUBLE</b>.

If the source <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> is of type VT_R8, this function extracts the <b>DOUBLE</b> value.

If the source <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> is not of type VT_R8, the function attempts to convert the value stored in the <b>VARIANT</b> structure into a <b>DOUBLE</b>. If a conversion is not possible, <a href="https://msdn.microsoft.com/en-us/library/Bb776598(v=VS.85).aspx">VariantToDouble</a> returns a failure code and sets <i>pdblRet</i> to <code>0.0</code>. See <a href="https://msdn.microsoft.com/en-us/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a> for a list of possible conversions. Of note, VT_EMPTY is successfully converted to 0.0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb776598(v=VS.85).aspx">VariantToDouble</a> to access a <b>DOUBLE</b> value stored in a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure.


```cpp
// VARIANT var;
// Assume variable var is initialize and valid.
// The application expects var to hold a VT_R8 value.
DOUBLE dblValue;

HRESULT hr = VariantToDouble(var, & dblValue);

if (SUCCEEDED(hr))
{
    // dblValue is now valid.
}
else
{
    // dblValue is always FALSE.
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762321(v=VS.85).aspx">InitVariantFromDouble</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776538(v=VS.85).aspx">PropVariantToDouble</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776599(v=VS.85).aspx">VariantToDoubleArray</a>
 

 

