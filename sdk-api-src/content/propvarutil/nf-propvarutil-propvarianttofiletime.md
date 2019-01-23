---
UID: NF:propvarutil.PropVariantToFileTime
title: PropVariantToFileTime function
author: windows-sdk-content
description: Extracts the FILETIME structure from a PROPVARIANT structure.
old-location: properties\PropVariantToFileTime.htm
tech.root: properties
ms.assetid: fc835395-8c2c-4f6a-88be-f438625442b9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PSTF_LOCAL, PSTF_UTC, PropVariantToFileTime, PropVariantToFileTime function [Windows Properties], _shell_PropVariantToFileTime, properties.PropVariantToFileTime, propvarutil/PropVariantToFileTime, shell.PropVariantToFileTime
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
 - PropVariantToFileTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantToFileTime function


## -description


Extracts the <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pstfOut [in]

Type: <b>PSTIME_FLAGS</b>

Specifies one of the following time flags.



#### PSTF_UTC (0)

Indicates the output will use coordinated universal time.



#### PSTF_LOCAL (1)

Indicates the output will use local time.


### -param pftOut [out]

Type: <b>FILETIME*</b>

          When this function returns, contains the extracted <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure. 
        


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a single filetime value. For instance, an application obtaining values from a property store can use this to safely extract a filetime value for filetime properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type VT_FILETIME or VT_DATE, this helper function extracts the value as a FILETIME using the timezone specified by <i>pstfOut</i>. If the source <b>PROPVARIANT</b> is VT_EMPTY or any other type, this function returns a failure result.

The source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> must be in Coordinated Universal Time (UTC). The PSTF_UTC and PSTF_LOCAL flags allow the calling application to specify what time zone the output should be converted to.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb776542(v=VS.85).aspx">PropVariantToFileTime</a> to access a FILETIME value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.


```cpp
// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore->GetValue(PKEY_DateModified, &propvar);
if (SUCCEEDED(hr))
{
     // PKEY_DateModified is expected to produce a VT_FILETIME or VT_EMPTY value.
     // PropVariantToFileTime will return a failure code for VT_EMPTY
     FILETIME ftModified;
     hr = PropVariantToFileTime(propvar, PSTF_UTC, &ftModified);
     if (SUCCEEDED(hr))
     {
        // ftModified is now valid and contains a file time in UTC
     }
     else
     {
        // Unable to convert propvar to a FILETIME
     }
     PropVariantClear(&propvar);
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762293(v=VS.85).aspx">InitPropVariantFromFileTime</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776543(v=VS.85).aspx">PropVariantToFileTimeVector</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776602(v=VS.85).aspx">VariantToFileTime</a>
 

 

