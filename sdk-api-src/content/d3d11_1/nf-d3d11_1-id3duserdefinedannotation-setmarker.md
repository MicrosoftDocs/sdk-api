---
UID: NF:d3d11_1.ID3DUserDefinedAnnotation.SetMarker
title: ID3DUserDefinedAnnotation::SetMarker (d3d11_1.h)
description: Marks a single point of execution in code.
helpviewer_keywords: ["ID3DUserDefinedAnnotation interface [Direct3D 11]","SetMarker method","ID3DUserDefinedAnnotation.SetMarker","ID3DUserDefinedAnnotation::SetMarker","SetMarker","SetMarker method [Direct3D 11]","SetMarker method [Direct3D 11]","ID3DUserDefinedAnnotation interface","d3d11_1/ID3DUserDefinedAnnotation::SetMarker","direct3d11.id3duserdefinedannotation_setmarker"]
old-location: direct3d11\id3duserdefinedannotation_setmarker.htm
tech.root: direct3d11
ms.assetid: EACF3660-C6A7-4C46-816C-0D9D292903B5
ms.date: 12/05/2018
ms.keywords: ID3DUserDefinedAnnotation interface [Direct3D 11],SetMarker method, ID3DUserDefinedAnnotation.SetMarker, ID3DUserDefinedAnnotation::SetMarker, SetMarker, SetMarker method [Direct3D 11], SetMarker method [Direct3D 11],ID3DUserDefinedAnnotation interface, d3d11_1/ID3DUserDefinedAnnotation::SetMarker, direct3d11.id3duserdefinedannotation_setmarker
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3DUserDefinedAnnotation::SetMarker
 - d3d11_1/ID3DUserDefinedAnnotation::SetMarker
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3DUserDefinedAnnotation.SetMarker
---

# ID3DUserDefinedAnnotation::SetMarker


## -description

Marks a single point of execution in code.

## -parameters

### -param Name [in]

A <b>NULL</b>-terminated <b>UNICODE</b> string that contains the name of the marker. The name is not relevant to the operating system. You can choose a name that is meaningful when the calling application is running under the Direct3D profiling tool.
A <b>NULL</b> pointer produces undefined results.

## -remarks

A user can visualize the marker when the calling application is running under an enabled Direct3D profiling tool such as Microsoft Visual Studio Ultimate 2012.

<b>SetMarker</b> has no effect if the calling application is not running under an enabled Direct3D profiling tool.


#### Examples

The following code shows how to use <b>SetMarker</b>.
          It also uses the <a href="/previous-versions/visualstudio/visual-studio-2010/ezzw7k98(v=vs.100)">CComPtr</a> smart pointer type.


```

CComPtr< ID3D11DeviceContext > pID3D11DeviceContext;

HRESULT hrCreateDevice = (*pfnD3D11CreateDevice)( 
        0,
        D3D_DRIVER_TYPE_NULL,
        0,
        0,
        NULL,
        0,
        D3D11_SDK_VERSION,
        NULL,
        0,
        & pID3D11DeviceContext );
VERIFY_SUCCEEDED(hrCreateDevice);

CComPtr<ID3DUserDefinedAnnotation> pPerf;
HRESULT hr = pID3D11DeviceContext->QueryInterface( __uuidof(pPerf), reinterpret_cast<void**>(&pPerf) );
if ( FAILED( hr ) ) 
    return;
pPerf->SetMarker( L”Occlusion test failed- not drawing sun flare” );

          
```


<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation">ID3DUserDefinedAnnotation</a>