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

# ID3DUserDefinedAnnotation::SetMarker


## -description


Marks a single point of execution in code.


## -parameters




### -param Name [in]

A <b>NULL</b>-terminated <b>UNICODE</b> string that contains the name of the marker. The name is not relevant to the operating system. You can choose a name that is meaningful when the calling application is running under the Direct3D profiling tool.
A <b>NULL</b> pointer produces undefined results.


## -returns



This method returns no values.




## -remarks



A user can visualize the marker when the calling application is running under an enabled Direct3D profiling tool such as Microsoft Visual Studio Ultimate 2012.

<b>SetMarker</b> has no effect if the calling application is not running under an enabled Direct3D profiling tool.


#### Examples


          The following code shows how to use <b>SetMarker</b>.
          It also uses the <a href="22d9ea8d-ed66-4c34-940f-141db11e83bd">CComPtr</a> smart pointer type.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
CComPtr&lt; ID3D11DeviceContext &gt; pID3D11DeviceContext;

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
        &amp; pID3D11DeviceContext );
VERIFY_SUCCEEDED(hrCreateDevice);

CComPtr&lt;ID3DUserDefinedAnnotation&gt; pPerf;
HRESULT hr = pID3D11DeviceContext-&gt;QueryInterface( __uuidof(pPerf), reinterpret_cast&lt;void**&gt;(&amp;pPerf) );
if ( FAILED( hr ) ) 
    return;
pPerf-&gt;SetMarker( L”Occlusion test failed- not drawing sun flare” );

          </pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/255DE24B-3D6D-49D9-B6A8-D296AB99B4C9">ID3DUserDefinedAnnotation</a>
 

 

