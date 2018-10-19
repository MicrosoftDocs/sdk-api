---
UID: NF:propvarutil.InitPropVariantFromFileTime
title: InitPropVariantFromFileTime function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on information stored in a FILETIME structure.
old-location: properties\InitPropVariantFromFileTime.htm
tech.root: properties
ms.assetid: 07c5ffe5-b2a5-46a3-969c-81201d9b8fdb
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: InitPropVariantFromFileTime, InitPropVariantFromFileTime function [Windows Properties], properties.InitPropVariantFromFileTime, propvarutil/InitPropVariantFromFileTime, shell.InitPropVariantFromFileTime, shell_InitPropVariantFromFileTime
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
 - InitPropVariantFromFileTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitPropVariantFromFileTime function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on information stored in a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


## -parameters




### -param pftIn [in]

Type: <b>const FILETIME*</b>

Pointer to the date and time as a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_FILETIME propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762293(v=VS.85).aspx">InitPropVariantFromFileTime</a>.


```cpp
FILETIME ft;
PROPVARIANT propvar;

GetSystemTimeAsFileTime(&ft);

HRESULT hr = InitPropVariantFromFileTime(&ft, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_FILETIME.
 
    PropVariantClear(&propvar);
}
```





## -see-also




<a href="https://msdn.microsoft.com/adf7ff5d-2d30-4490-9868-9ad78ef7a0b6">GetSystemTimeAsFileTime</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762294(v=VS.85).aspx">InitPropVariantFromFileTimeVector</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762323(v=VS.85).aspx">InitVariantFromFileTime</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776542(v=VS.85).aspx">PropVariantToFileTime</a>
 

 

