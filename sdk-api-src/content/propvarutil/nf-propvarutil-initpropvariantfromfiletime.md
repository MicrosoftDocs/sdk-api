---
UID: NF:propvarutil.InitPropVariantFromFileTime
title: InitPropVariantFromFileTime function (propvarutil.h)
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on information stored in a FILETIME structure.
old-location: properties\InitPropVariantFromFileTime.htm
tech.root: properties
ms.assetid: 07c5ffe5-b2a5-46a3-969c-81201d9b8fdb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromFileTime, InitPropVariantFromFileTime function [Windows Properties], properties.InitPropVariantFromFileTime, propvarutil/InitPropVariantFromFileTime, shell.InitPropVariantFromFileTime, shell_InitPropVariantFromFileTime
ms.topic: function
f1_keywords: 
 - "propvarutil/InitPropVariantFromFileTime"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# InitPropVariantFromFileTime function


## -description


Initializes a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on information stored in a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.


## -parameters




### -param pftIn [in]

Type: <b>const FILETIME*</b>

Pointer to the date and time as a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.


### -param ppropvar [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_FILETIME propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromfiletime">InitPropVariantFromFileTime</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime">GetSystemTimeAsFileTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromfiletimevector">InitPropVariantFromFileTimeVector</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromfiletime">InitVariantFromFileTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttofiletime">PropVariantToFileTime</a>
 

 

