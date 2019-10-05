---
UID: NF:propvarutil.InitPropVariantFromResource
title: InitPropVariantFromResource function (propvarutil.h)
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a string resource embedded in an executable file.
old-location: properties\InitPropVariantFromResource.htm
tech.root: properties
ms.assetid: c958f823-f820-4b0b-86ed-84ad18befbd1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromResource, InitPropVariantFromResource function [Windows Properties], properties.InitPropVariantFromResource, propvarutil/InitPropVariantFromResource, shell.InitPropVariantFromResource, shell_InitPropVariantFromResource
ms.topic: function
f1_keywords: 
 - "propvarutil/InitPropVariantFromResource"
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
 - InitPropVariantFromResource
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# InitPropVariantFromResource function


## -description


Initializes a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure based on a string resource embedded in an executable file.


## -parameters




### -param hinst [in]

Type: <b>HINSTANCE</b>

Handle to an instance of the module whose executable file contains the string resource.


### -param id [in]

Type: <b>UINT</b>

Integer identifier of the string to be loaded.


### -param ppropvar [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function creates a VT_LPWSTR propvariant. If the specified resource does not exist, it initializes the <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> with an empty string. Resource strings longer than 1024 characters are truncated and null-terminated.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromresource">InitPropVariantFromResource</a>.


```cpp
// HINSTANCE hinst;
// UINT id;
// Assume variables hinst and id are initialized and valid.
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromResource(hinst, id, &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_LPWSTR.
    PropVariantClear(&propvar);
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstring">InitPropVariantFromString</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromresource">InitVariantFromResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-loadstringa">LoadString</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostring">PropVariantToString</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringwithdefault">PropVariantToStringWithDefault</a>
 

 

