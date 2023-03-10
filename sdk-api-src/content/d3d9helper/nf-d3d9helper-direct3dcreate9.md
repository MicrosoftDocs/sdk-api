---
UID: NF:d3d9helper.Direct3DCreate9
title: Direct3DCreate9 function (d3d9helper.h)
description: The Direct3DCreate9 function (d3d9helper.h) creates an IDirect3D9 object and return an interface to it.
helpviewer_keywords: ["911c767b-a75f-146e-b3ba-02c1df537127","Direct3DCreate9","Direct3DCreate9 function [Direct3D 9]","d3d9helper/Direct3DCreate9","direct3d9.direct3dcreate9"]
old-location: direct3d9\direct3dcreate9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\direct3d_tutorials.htm
ms.date: 08/11/2022
ms.keywords: 911c767b-a75f-146e-b3ba-02c1df537127, Direct3DCreate9, Direct3DCreate9 function [Direct3D 9], d3d9helper/Direct3DCreate9, direct3d9.direct3dcreate9
req.header: d3d9helper.h
req.include-header: D3D9.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3d9.lib
req.dll: D3d9.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Direct3DCreate9
 - d3d9helper/Direct3DCreate9
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3d9.dll
 - Ext-MS-Win-dx-d3d9-l1-1-0.dll
api_name:
 - Direct3DCreate9
---

# Direct3DCreate9 function


## -description

Create an IDirect3D9 object and return an interface to it.

## -parameters

### -param SDKVersion

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The value of this parameter should be D3D_SDK_VERSION. See Remarks.

## -returns

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a>*</b>

If successful, this function returns a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a> interface; otherwise, a <b>NULL</b> pointer is returned.

## -remarks

The Direct3D object is the first Direct3D COM object that your graphical application needs to create and the last object that your application needs to release. Functions for enumerating and retrieving capabilities of a device are accessible through the Direct3D object. This enables applications to select devices without creating them.

Create an IDirect3D9 object as shown here:


```

LPDIRECT3D9 g_pD3D = NULL;
    
if( NULL == (g_pD3D = Direct3DCreate9(D3D_SDK_VERSION)))
    return E_FAIL;

```


The IDirect3D9 interface supports enumeration of active display adapters and allows the creation of <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a> objects. If the user dynamically adds adapters (either by adding devices to the desktop, or by hot-docking a laptop), those devices will not be included in the enumeration. Creating a new IDirect3D9 interface will expose the new devices.

D3D_SDK_VERSION is passed to this function to ensure that the header files against which an application is compiled match the version of the runtime DLL's that are installed on the machine. D3D_SDK_VERSION is only changed in the runtime when a header change (or other code change) would require an application to be rebuilt. If this function fails, it indicates that the header file version does not match the runtime DLL version.

For an example, see <a href="/windows/desktop/direct3d9/creating-a-device">Creating a Device (Direct3D 9)</a>.

## -see-also

<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-functions">Direct3D Functions</a>
