---
UID: NF:mfidl.MFLoadSignedLibrary
title: MFLoadSignedLibrary function (mfidl.h)
description: Loads a dynamic link library that is signed for the protected environment.
helpviewer_keywords: ["MFLoadSignedLibrary","MFLoadSignedLibrary function [Media Foundation]","mf.mfloadsignedlibrary","mfidl/MFLoadSignedLibrary"]
old-location: mf\mfloadsignedlibrary.htm
tech.root: mf
ms.assetid: 979A5FE5-0DED-4C5A-A27D-CDD10A4A8D5C
ms.date: 12/05/2018
ms.keywords: MFLoadSignedLibrary, MFLoadSignedLibrary function [Media Foundation], mf.mfloadsignedlibrary, mfidl/MFLoadSignedLibrary
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFLoadSignedLibrary
 - mfidl/MFLoadSignedLibrary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFLoadSignedLibrary
---

# MFLoadSignedLibrary function


## -description

Loads a dynamic link library that is signed for the protected environment.

## -parameters

### -param pszName [in]

The name of the dynamic link library to load.  This dynamic link library must be signed for the protected environment.

### -param ppLib [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsignedlibrary">IMFSignedLibrary</a> interface for the library.

## -remarks

A singlemodule load count is maintained on the dynamic link library (as it is with <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>).  This load count  is freed when the final release is called on the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsignedlibrary">IMFSignedLibrary</a> object.


#### Examples

The following example demonstrates how to load a signed library and retrieve the address of a function in that library. 


```cpp
IMFSignedLibrary *pLib;
hr = MFLoadSignedLibrary(TEST_PELOAD_FILE, &pLib);
if (SUCCEEDED(hr))
{
    PVOID functionAddress;
    hr = pLib->GetProcedureAddress("myFunctionName", &functionAddress);
}
//  Unload the library
pLib->Release();

```

## -see-also

<a href="/windows/desktop/api/mfidl/nf-mfidl-imfsignedlibrary-getprocedureaddress">GetProcedureAddress</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsignedlibrary">IMFSignedLibrary</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>