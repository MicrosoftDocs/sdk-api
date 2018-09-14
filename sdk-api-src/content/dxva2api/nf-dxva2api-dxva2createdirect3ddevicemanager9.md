---
UID: NF:dxva2api.DXVA2CreateDirect3DDeviceManager9
title: DXVA2CreateDirect3DDeviceManager9 function
author: windows-sdk-content
description: Creates an instance of the Direct3D Device Manager.
old-location: mf\dxva2createdirect3ddevicemanager9.htm
tech.root: medfound
ms.assetid: b06e9c68-80ee-4997-bcf7-f05879aa5776
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: DXVA2CreateDirect3DDeviceManager9, DXVA2CreateDirect3DDeviceManager9 function [Media Foundation], b06e9c68-80ee-4997-bcf7-f05879aa5776, dxva2api/DXVA2CreateDirect3DDeviceManager9, mf.dxva2createdirect3ddevicemanager9
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - DXVA2CreateDirect3DDeviceManager9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DXVA2CreateDirect3DDeviceManager9 function


## -description


Creates an instance of the <a href="https://msdn.microsoft.com/d82fd82d-510e-4004-b18b-8f2372e29701">Direct3D Device Manager</a>.
        


## -parameters




### -param pResetToken [out]

Receives a token that identifies this instance of the Direct3D device manager. Use this token when calling <a href="https://msdn.microsoft.com/01d2c2ea-5967-4a2d-9c78-e6e8b42a7e33">IDirect3DDeviceManager9::ResetDevice</a>.
          


### -param ppDeviceManager [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/e661e666-dc51-4a71-9ecd-62a667bb217d">IDirect3DDeviceManager9</a> interface. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Windows Store apps must use <a href="https://msdn.microsoft.com/4A0DC266-FCF0-4ECD-AC78-CF429839486D">IMFDXGIDeviceManager</a> and <a href="https://msdn.microsoft.com/7C91BEB9-53D2-4799-98F8-2B92128E37C3">Direct3D 11 Video APIs</a>. 


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CreateD3DDeviceManager(
    IDirect3DDevice9 *pDevice, 
    UINT *pReset, 
    IDirect3DDeviceManager9 **ppManager
    )
{
    UINT resetToken = 0;

    IDirect3DDeviceManager9 *pD3DManager = NULL;

    HRESULT hr = DXVA2CreateDirect3DDeviceManager9(&amp;resetToken, &amp;pD3DManager);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pD3DManager-&gt;ResetDevice(pDevice, resetToken);

    if (FAILED(hr))
    {
        goto done;
    }

    *ppManager = pD3DManager;
    (*ppManager)-&gt;AddRef();

    *pReset = resetToken;


done:
    SafeRelease(&amp;pD3DManager);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d82fd82d-510e-4004-b18b-8f2372e29701">Direct3D Device Manager</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

