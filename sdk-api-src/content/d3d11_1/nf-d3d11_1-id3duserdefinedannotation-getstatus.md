---
UID: NF:d3d11_1.ID3DUserDefinedAnnotation.GetStatus
title: ID3DUserDefinedAnnotation::GetStatus (d3d11_1.h)
description: Determines whether the calling application is running under a Microsoft Direct3D profiling tool.
helpviewer_keywords: ["GetStatus","GetStatus method [Direct3D 11]","GetStatus method [Direct3D 11]","ID3DUserDefinedAnnotation interface","ID3DUserDefinedAnnotation interface [Direct3D 11]","GetStatus method","ID3DUserDefinedAnnotation.GetStatus","ID3DUserDefinedAnnotation::GetStatus","d3d11_1/ID3DUserDefinedAnnotation::GetStatus","direct3d11.id3duserdefinedannotation_getstatus"]
old-location: direct3d11\id3duserdefinedannotation_getstatus.htm
tech.root: direct3d11
ms.assetid: 67C95617-3454-4457-AB3B-FD79C176E314
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Direct3D 11], GetStatus method [Direct3D 11],ID3DUserDefinedAnnotation interface, ID3DUserDefinedAnnotation interface [Direct3D 11],GetStatus method, ID3DUserDefinedAnnotation.GetStatus, ID3DUserDefinedAnnotation::GetStatus, d3d11_1/ID3DUserDefinedAnnotation::GetStatus, direct3d11.id3duserdefinedannotation_getstatus
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
 - ID3DUserDefinedAnnotation::GetStatus
 - d3d11_1/ID3DUserDefinedAnnotation::GetStatus
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
 - ID3DUserDefinedAnnotation.GetStatus
---

# ID3DUserDefinedAnnotation::GetStatus


## -description

Determines whether the calling application is running under a Microsoft Direct3D profiling tool.



## -returns

The return value is nonzero if the calling application is running under a Direct3D profiling tool such as Visual Studio Ultimate 2012, and zero otherwise.

## -remarks

You can call <b>GetStatus</b> to determine whether your application is running under a Direct3D profiling tool before you make further calls to other methods of the <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation">ID3DUserDefinedAnnotation</a> interface. For example, the <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3duserdefinedannotation-beginevent">ID3DUserDefinedAnnotation::BeginEvent</a> and <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3duserdefinedannotation-endevent">ID3DUserDefinedAnnotation::EndEvent</a> methods have no effect if the calling application is not running under an enabled Direct3D profiling tool. Therefore, you do not need to call these methods unless your application is running under a Direct3D profiling tool.


#### Examples

The following code shows how to use <b>GetStatus</b>.
          


```

#ifdef DEVELOPMENT_BUILD
    if ( pPerf->GetStatus() )
        m_MakeD3DAnnotationCalls = true;
#endif

…

   if ( m_ MakeD3DAnnotationCalls )
        pPerf->BeginEvent(L“Drawing Ocean”);
   MyDrawOceanRoutine();

          
```


<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation">ID3DUserDefinedAnnotation</a>
