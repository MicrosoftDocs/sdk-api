---
UID: NF:propvarutil.PropVariantToDoubleWithDefault
title: PropVariantToDoubleWithDefault function
author: windows-sdk-content
description: Extracts a double property value of a PROPVARIANT structure. If no value exists, then the specified default value is returned.
old-location: properties\PropVariantToDoubleWithDefault.htm
tech.root: properties
ms.assetid: 81584e13-0ef7-47ce-b78f-b4a79712ff1e
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: PropVariantToDoubleWithDefault, PropVariantToDoubleWithDefault function [Windows Properties], properties.PropVariantToDoubleWithDefault, propvarutil/PropVariantToDoubleWithDefault, shell.PropVariantToDoubleWithDefault, shell_PropVariantToDoubleWithDefault
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
 - PropVariantToDoubleWithDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantToDoubleWithDefault function


## -description


Extracts a double property value of a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. If no value exists, then the specified default value is returned.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param dblDefault [in]

Type: <b>DOUBLE</b>

Specifies default property value, for use where no value currently exists.


## -returns



Type: <b>DOUBLE</b>

Returns extracted <b>double</b> value, or default.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a double value and would like to use a default value if it does not. For instance, an application obtaining values from a property store can use this to safely extract the double value for double properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_R8</b>, this helper function extracts the double value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a double. If the source <b>PROPVARIANT</b> has type <b>VT_EMPTY</b> or a conversion is not possible, then <a href="shell.PropVariantToDoubleWithDefault">PropVariantToDoubleWithDefault</a> will return the default provided by <i>dblDefault</i>. See <a href="shell.PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions.


#### Examples


```cpp
// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore->GetValue(PKEY_Image_HorizontalResolution, &propvar);
if (SUCCEEDED(hr))
{
     // PKEY_Image_HorizontalResolution is expected to produce a VT_R8 or VT_EMPTY value.
     // The application developer decided to treat VT_EMPTY or invalid values as 72.0
     DOUBLE dblResolution = PropVariantToDoubleWithDefault(propvar, 72.0);
     // dblResolution is now valid.
     PropVariantClear(&propvar);
}
```





## -see-also




<a href="shell.InitPropVariantFromDouble">InitPropVariantFromDouble</a>



<a href="shell.PropVariantChangeType">PropVariantChangeType</a>



<a href="shell.PropVariantToDoubleVector">PropVariantToDoubleVector</a>



<a href="shell.VariantToDouble">VariantToDouble</a>
 

 

