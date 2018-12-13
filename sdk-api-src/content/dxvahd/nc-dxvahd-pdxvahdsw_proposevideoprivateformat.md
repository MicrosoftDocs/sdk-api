---
UID: NC:dxvahd.PDXVAHDSW_ProposeVideoPrivateFormat
title: PDXVAHDSW_ProposeVideoPrivateFormat
author: windows-sdk-content
description: Gets a private surface format from a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\pdxvahdsw_proposevideoprivateformat.htm
tech.root: medfound
ms.assetid: b543f05f-40fc-4bdf-ae53-9a451d3bdf2a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PDXVAHDSW_ProposeVideoPrivateFormat, PDXVAHDSW_ProposeVideoPrivateFormat callback, PDXVAHDSW_ProposeVideoPrivateFormat callback function [Media Foundation], dxvahd/PDXVAHDSW_ProposeVideoPrivateFormat, mf.pdxvahdsw_proposevideoprivateformat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dxvahd.h
api_name:
 - PDXVAHDSW_ProposeVideoPrivateFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDXVAHDSW_ProposeVideoPrivateFormat callback function


## -description


Gets a private surface format from a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param hDevice [in]

A handle to the plug-in DXVA-HD device.


### -param *pFormat [in, out]

A pointer to a <b>D3DFORMAT</b> value. On input, specifies the surface format that is requested by the application. On output, specifies the private surface format that the plug-in device proposes.


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is called when the application calls <a href="https://msdn.microsoft.com/c467a077-104c-443d-896b-d69441aa5160">IDXVAHD_Device::CreateVideoSurface</a>  if  the following conditions are true:

<ul>
<li>The type of input surface is <b>DXVAHD_SURFACE_TYPE_VIDEO_INPUT_PRIVATE</b>.</li>
<li>The Direct3D device does not support the surface format requested by the application natively.</li>
</ul>
This function enbles the plug-in device  to propose an alternate format with an equivalent memory layout. For example, if the application requests AYUV, the plug-in device might allocate a surface of type <b>D3DFMT_A8R8G8B8</b>.

If the function succeeds, the <a href="https://msdn.microsoft.com/c467a077-104c-443d-896b-d69441aa5160">CreateVideoSurface</a> method attempts to create a surface with the format returned in <i>pFormat</i>. 


#### Examples

The following code shows how a plug-in device proposes <b>D3DFMT_A8R8G8B8</b> as an alternative surface format for AYUV. 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HRESULT CALLBACK ProposeVideoPrivateFormat(
    HANDLE hDevice,
    D3DFORMAT* pFormat 
    )
{
    switch (*pFormat)
    {
        case D3DFMT_AYUV: 
            *pFormat = D3DFMT_A8R8G8B8; 
            return S_OK;

        default: 
            return E_FAIL;
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/74c329cc-af54-4cf8-8cb6-eed9e96db4c5">DXVAHDSW_CALLBACKS</a>



<a href="https://msdn.microsoft.com/c467a077-104c-443d-896b-d69441aa5160">IDXVAHD_Device::CreateVideoSurface</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

