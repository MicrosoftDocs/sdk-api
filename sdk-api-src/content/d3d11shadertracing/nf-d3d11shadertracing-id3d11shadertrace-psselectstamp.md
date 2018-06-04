---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D11ShaderTrace::PSSelectStamp


## -description


Sets the specified pixel-shader stamp.


## -parameters




### -param stampIndex [in]

The index of the stamp to select.


## -returns



<b>PSSelectStamp</b> returns:
        <ul>
<li><b>S_OK</b> if the method set the pixel-shader stamp, and if the primitive covers the pixel and sample for the stamp.</li>
<li><b>S_FALSE</b> if the method set the pixel-shader stamp, and if the invocation for the selected stamp falls off the primitive.</li>
<li><b>E_FAIL</b> if you called the method for a vertex shader or geometry shader;   <b>PSSelectStamp</b> is meaningful only for pixel shaders.</li>
<li><b>E_INVALIDARG</b> if <i>stampIndex</i> is out of range [0..3].</li>
<li>Possibly other error codes that are described in <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.</li>
</ul>





## -remarks



After you call <b>PSSelectStamp</b> to set the pixel-shader stamp, you can call the <a href="https://msdn.microsoft.com/35BC4F23-64E0-4E45-A621-925A5CA20AFE">ID3D11ShaderTrace::GetInitialRegisterContents</a>,  <a href="https://msdn.microsoft.com/ECEF965F-D046-4F84-A205-F9666ECAE08C">ID3D11ShaderTrace::GetStep</a>, <a href="https://msdn.microsoft.com/360BB797-D5A9-486A-94ED-AF1CD3A4E118">ID3D11ShaderTrace::GetWrittenRegister</a>, and <a href="https://msdn.microsoft.com/2BDA0C25-B5D7-4A8D-A762-2C3FDF113433">ID3D11ShaderTrace::GetReadRegister</a> methods to get trace data for that stamp.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/27FF1E53-262A-4642-A4A8-7E21163C6DF9">ID3D11ShaderTrace</a>
 

 

