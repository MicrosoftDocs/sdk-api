---
UID: NF:d3d11.ID3D11DeviceContext.RSGetViewports
title: ID3D11DeviceContext::RSGetViewports
author: windows-sdk-content
description: Gets the array of viewports bound to the rasterizer stage.
old-location: direct3d11\id3d11devicecontext_rsgetviewports.htm
tech.root: direct3d11
ms.assetid: 9932182f-8e62-41fe-9004-7fb0b591630f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 19831c51-f6c4-f65f-6ada-c90fa97f0a32, ID3D11DeviceContext interface [Direct3D 11],RSGetViewports method, ID3D11DeviceContext.RSGetViewports, ID3D11DeviceContext::RSGetViewports, RSGetViewports, RSGetViewports method [Direct3D 11], RSGetViewports method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::RSGetViewports, direct3d11.id3d11devicecontext_rsgetviewports
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.RSGetViewports
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::RSGetViewports


## -description


Gets the array of viewports bound to the rasterizer stage.


## -parameters




### -param pNumViewports [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

A pointer to a variable that, on input, specifies the number of viewports (ranges from 0 to <b>D3D11_VIEWPORT_AND_SCISSORRECT_OBJECT_COUNT_PER_PIPELINE</b>)
            in the <i>pViewports</i> array; on output, the variable contains the actual number of viewports that are bound to the rasterizer stage.
            If <i>pViewports</i> is <b>NULL</b>, <b>RSGetViewports</b> fills the variable with the number of viewports currently bound.

<div class="alert"><b>Note</b>  In some versions of the Windows SDK, a <a href="overviews_direct3d_11_devices_layers.htm">debug device</a> will raise an exception if the input value in the variable to which <i>pNumViewports</i> points is greater than <b>D3D11_VIEWPORT_AND_SCISSORRECT_OBJECT_COUNT_PER_PIPELINE</b> even if <i>pViewports</i> is <b>NULL</b>.  The regular runtime ignores the value in the variable to which <i>pNumViewports</i> points when <i>pViewports</i> is <b>NULL</b>.  This behavior of a debug device might be corrected in a future release of the Windows SDK.
            </div>
<div> </div>

### -param pViewports [out, optional]

Type: <b><a href="https://msdn.microsoft.com/7ef29e40-4b42-4794-83b6-44581c0d529f">D3D11_VIEWPORT</a>*</b>

An array of <a href="https://msdn.microsoft.com/7ef29e40-4b42-4794-83b6-44581c0d529f">D3D11_VIEWPORT</a> structures for the viewports that are bound to the rasterizer stage. If the number of viewports (in the variable to which <i>pNumViewports</i> points) is
            greater than the actual number of viewports currently bound, unused elements of the array contain 0.
            For info about how the viewport size depends on the device <a href="overviews_direct3d_11_devices_downlevel_intro.htm">feature level</a>, which has changed between Direct3D 11
            and Direct3D 10, see <b>D3D11_VIEWPORT</b>.
          


## -returns



Returns nothing.




## -remarks



<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

