---
UID: NN:d3d11_1.ID3DUserDefinedAnnotation
title: ID3DUserDefinedAnnotation (d3d11_1.h)
description: The ID3DUserDefinedAnnotation interface enables an application to describe conceptual sections and markers within the application's code flow.
helpviewer_keywords: ["ID3DUserDefinedAnnotation","ID3DUserDefinedAnnotation interface [Direct3D 11]","ID3DUserDefinedAnnotation interface [Direct3D 11]","described","d3d11_1/ID3DUserDefinedAnnotation","direct3d11.id3duserdefinedannotation"]
old-location: direct3d11\id3duserdefinedannotation.htm
tech.root: direct3d11
ms.assetid: 255DE24B-3D6D-49D9-B6A8-D296AB99B4C9
ms.date: 12/05/2018
ms.keywords: ID3DUserDefinedAnnotation, ID3DUserDefinedAnnotation interface [Direct3D 11], ID3DUserDefinedAnnotation interface [Direct3D 11],described, d3d11_1/ID3DUserDefinedAnnotation, direct3d11.id3duserdefinedannotation
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
 - ID3DUserDefinedAnnotation
 - d3d11_1/ID3DUserDefinedAnnotation
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
 - ID3DUserDefinedAnnotation
---

# ID3DUserDefinedAnnotation interface


## -description

The <b>ID3DUserDefinedAnnotation</b> interface enables an application to describe conceptual sections and markers within the application's code flow. An appropriately enabled tool, such as Microsoft Visual Studio Ultimate 2012, can display these sections and markers visually along the tool's Microsoft Direct3D time line, while the tool debugs the application. These visual notes allow users of such a tool to navigate to parts of the time line that are of interest, or to understand what set of Direct3D calls are produced by certain sections of the application's code.

## -inheritance

The <b>ID3DUserDefinedAnnotation</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3DUserDefinedAnnotation</b> also has these types of members:

## -remarks

The methods of <b>ID3DUserDefinedAnnotation</b> have no effect when the calling application is not running under a Direct3D-specific profiling tool like Visual Studio Ultimate 2012.


The <b>ID3DUserDefinedAnnotation</b> interface is published by Microsoft Direct3D 11 device contexts. Therefore, <b>ID3DUserDefinedAnnotation</b> has the same threading rules as the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> interface, or any other context interface. For more information about Direct3D threading, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread">MultiThreading</a>.
To retrieve the <b>ID3DUserDefinedAnnotation</b> interface for the context, call the <b>QueryInterface</b> method for the context (for example, <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">ID3D11DeviceContext::QueryInterface</a>). In this call, you must pass the identifier of <b>ID3DUserDefinedAnnotation</b>. 

The <b>ID3DUserDefinedAnnotation</b> interface is the Microsoft Direct3D 10 and later equivalent of the Direct3D 9 <a href="https://msdn.microsoft.com/library/ee417071(v=VS.85).aspx">PIX functions</a> (D3DPERF_* functions).

<div class="alert"><b>Note</b>  Setting the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag">D3D11_CREATE_DEVICE_PREVENT_ALTERING_LAYER_SETTINGS_FROM_REGISTRY</a> flag in your app replaces calling D3DPerf_SetOptions(1). But, to prevent Direct3D debugging tools from hooking your app, your app can also call <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3duserdefinedannotation-getstatus">ID3DUserDefinedAnnotation::GetStatus</a> to determine whether it is running under a Direct3D debugging tool and then exit accordingly.</div>
<div> </div>
You must call the <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3duserdefinedannotation-beginevent">BeginEvent</a> and <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3duserdefinedannotation-endevent">EndEvent</a> methods in pairs; pairs of calls to these methods can nest within pairs of calls to these methods at a higher level in the application's call stack.  In other words, a "Draw World" section can entirely contain another section named "Draw Trees," which can in turn entirely contain a section called "Draw Oaks." You can only associate an <b>EndEvent</b> method with the most recent <b>BeginEvent</b> method, that is, pairs cannot overlap. You cannot call an <b>EndEvent</b> for any <b>BeginEvent</b> that preceded the most recent <b>BeginEvent</b>. In fact, the runtime interprets the first <b>EndEvent</b> as ending the second <b>BeginEvent</b>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-common-interfaces">Common Version Interfaces</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
