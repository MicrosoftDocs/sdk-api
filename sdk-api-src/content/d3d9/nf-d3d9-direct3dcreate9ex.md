---
UID: NF:d3d9.Direct3DCreate9Ex
title: Direct3DCreate9Ex function (d3d9.h)
description: Creates an IDirect3D9Ex object and returns an interface to it.
helpviewer_keywords: ["Direct3DCreate9Ex","Direct3DCreate9Ex function [Direct3D 9]","d3bc9dd0-05d5-c0a2-6b7c-7e11497d0e97","d3d9/Direct3DCreate9Ex","direct3d9.direct3dcreate9ex"]
old-location: direct3d9\direct3dcreate9ex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\direct3dcreate9.htm
ms.date: 12/05/2018
ms.keywords: Direct3DCreate9Ex, Direct3DCreate9Ex function [Direct3D 9], d3bc9dd0-05d5-c0a2-6b7c-7e11497d0e97, d3d9/Direct3DCreate9Ex, direct3d9.direct3dcreate9ex
req.header: d3d9.h
req.include-header: 
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
 - Direct3DCreate9Ex
 - d3d9/Direct3DCreate9Ex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3d9.dll
 - Ext-MS-Win-DX-D3D9-L1-1-0.dll
api_name:
 - Direct3DCreate9Ex
---

# Direct3DCreate9Ex function


## -description

Creates an <a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex">IDirect3D9Ex</a> object and returns an interface to it.

## -parameters

### -param SDKVersion [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The value of this parameter should be <b>D3D_SDK_VERSION</b>. See Remarks.

### -param unnamedParam2 [out]

Type: <b><a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex">IDirect3D9Ex</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex">IDirect3D9Ex</a> interface, representing the
          created <b>IDirect3D9Ex</b> object. If the function fails, <b>NULL</b> is inserted here.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

<ul>
<li><b>D3DERR_NOTAVAILABLE</b> if Direct3DEx features are not supported (no WDDM driver is
            installed) or if the <b>SDKVersion</b> does not match the version of the DLL.</li>
<li><b>D3DERR_OUTOFMEMORY</b> if out-of-memory conditions are detected when creating the
            enumerator object.</li>
<li><b>S_OK</b> if the creation of the enumerator object is successful.</li>
</ul>

## -remarks

The <a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex">IDirect3D9Ex</a> object is the first object that the application creates and the
        last object that the application releases. Functions for enumerating and retrieving
        capabilities of a device are accessible through the <b>IDirect3D9Ex</b> object.
        This enables applications to select devices without creating them.

The <a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex">IDirect3D9Ex</a> interface supports enumeration of active display adapters
        and allows the creation of <b>IDirect3D9Ex</b> objects. If the user dynamically adds
        adapters (either by adding devices to the desktop, or by hot-docking a laptop), these
        devices are not included in the enumeration. Creating a new <b>IDirect3D9Ex</b> interface will expose the new devices.

Pass the <b>D3D_SDK_VERSION</b> flag to this function to ensure that header files used in the
        compiled application match the version of the installed runtime DLLs. <b>D3D_SDK_VERSION
        </b> is changed in the runtime only when a header or another code change would require
        rebuilding the application. If this function fails, it indicates that the versions of the
        header file and the runtime DLL do not match.

<div class="alert"><b>Note</b>  <b>Direct3DCreate9Ex</b> is supported only in Windows Vista, Windows Server 2008, and Windows 7.  
        Earlier versions of the D3D9.dll library do not include <a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex">Direct3D9Ex</a> and <b>Direct3DCreate9Ex</b>.</div>
<div> </div>

#### Examples

Creating an IDirect3D9Ex object.

The following code example demonstrates how to create an <a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex">IDirect3D9Ex</a> object
          using <b>Direct3DCreate9Ex</b>.  This example then uses the <b>IDirect3D9Ex</b> object to 
    create an <a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a> object, which is returned as an out parameter to
    the function.

<div class="code"></div>

```cpp
HRESULT InitD3D9Ex( /* IN */ HWND hWnd, /* OUT */ IDirect3DDevice9Ex ** ppD3DDevice )
{
    HRESULT hr = E_FAIL;
    IDirect3D9Ex * pD3D = NULL;
    IDirect3DDevice9Ex * pDevice = NULL;

    if(ppD3DDevice == NULL)
    {
        return hr;
    }
    
    // Create the D3D object, which is needed to create the D3DDevice.
    if(FAILED(hr = Direct3DCreate9Ex( D3D_SDK_VERSION, &pD3D )))
    {
        *ppD3DDevice = NULL;
        return hr;
    }
        
        
    // Set up the structure used to create the D3DDevice. 
    D3DPRESENT_PARAMETERS d3dpp; 
    ZeroMemory( &d3dpp, sizeof(d3dpp) );
    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_DISCARD;
    d3dpp.BackBufferFormat = D3DFMT_UNKNOWN;

    // Create the Direct3D device. 
    if( FAILED( hr = pD3D->CreateDeviceEx( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                      &d3dpp, NULL, &pDevice ) ) )

    {
        *ppD3DDevice = NULL;
        return hr;
    }

    // Device state would normally be set here

    *ppD3DDevice = pDevice;

    return hr;
}

```


Checking for Direct3D9Ex.

The following code example demonstrates how to check for the existence of <b>Direct3DCreate9Ex</b> and fail on platforms that do not support it. You can use this code in a game launcher to present 
    an error message to the user or to load a renderer that uses the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a> interface instead.

To check for <b>Direct3DCreate9Ex</b>, this example explicitly loads the D3D9.dll
          library using the Win32 <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function.  The example then assigns the
          address of <b>Direct3DCreate9Ex</b> to a pointer by using the Win32 <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> function.  If <b>Direct3DCreate9Ex</b> is not present, the function pointer is <b>NULL</b>,
          and the code example returns an <b>ERROR_NOT_SUPPORTED  </b><b>HRESULT</b> value.
          However, if <b>Direct3DCreate9Ex</b> is present, it returns an <b>S_OK</b> value.

<div class="code"></div>

```cpp
HRESULT CheckD3D9Ex( void )
{
    HRESULT hr = E_FAIL;
    HMODULE libHandle = NULL;

    // Manually load the d3d9.dll library.
    libHandle = LoadLibrary(L"d3d9.dll");

    if(libHandle != NULL)
    {
        // Define a function pointer to the Direct3DCreate9Ex function.
        typedef HRESULT (WINAPI *LPDIRECT3DCREATE9EX)( UINT, void **);

        // Obtain the address of the Direct3DCreate9Ex function. 
        LPDIRECT3DCREATE9EX Direct3DCreate9ExPtr = NULL;
            
        Direct3DCreate9ExPtr = (LPDIRECT3DCREATE9EX)GetProcAddress( libHandle, "Direct3DCreate9Ex" );

        if ( Direct3DCreate9ExPtr != NULL)
        {
            // Direct3DCreate9Ex is supported.
            hr = S_OK;
        }
        else
        {
            // Direct3DCreate9Ex is not supported on this
            // operating system.
            hr = ERROR_NOT_SUPPORTED;
        }

        // Free the library.
        FreeLibrary( libHandle );

    }

    
    return hr;
}

```


Note that you may cast an <a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a> interface pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a> interface pointer because the extended version is inherited. This makes it possible to use the extended device with existing Direct3D 9 code, except where the new device changes the semantics of the interface.  For more information about differences between the two interfaces, see <a href="/windows/desktop/direct3d9/dx9lh">device behavior changes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-functions">Direct3D Functions</a>