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

# ID3DUserDefinedAnnotation::BeginEvent


## -description


Marks the beginning of a section of event code.


## -parameters




### -param Name [in]

A <b>NULL</b>-terminated <b>UNICODE</b> string that contains the name of the event. The name is not relevant to the operating system. You can choose a name that is meaningful when the calling application is running under the Direct3D profiling tool.
A <b>NULL</b> pointer produces undefined results.


## -returns



Returns the number of previous calls to <b>BeginEvent</b> that have not yet been finalized by calls to the <a href="https://msdn.microsoft.com/5C478278-EC05-4214-80F9-808EADA76E41">ID3DUserDefinedAnnotation::EndEvent</a> method.

The return value is –1 if the calling application is not running under a Direct3D profiling tool.




## -remarks



You call the <a href="https://msdn.microsoft.com/5C478278-EC05-4214-80F9-808EADA76E41">EndEvent</a> method to mark the end of the section of event code.

A user can visualize the event when the calling application is running under an enabled Direct3D profiling tool such as Microsoft Visual Studio Ultimate 2012.

<b>BeginEvent</b> has no effect if the calling application is not running under an enabled Direct3D profiling tool.


#### Examples


          The following code shows how to use a pair of calls to the <b>BeginEvent</b> and <a href="https://msdn.microsoft.com/5C478278-EC05-4214-80F9-808EADA76E41">EndEvent</a> methods.
          It also uses the <a href="22d9ea8d-ed66-4c34-940f-141db11e83bd">CComPtr</a> smart pointer type.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
CComPtr&lt; ID3D11DeviceContext &gt; pContext;

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
        &amp; pContext );
VERIFY_SUCCEEDED(hrCreateDevice);
CComPtr&lt;ID3DUserDefinedAnnotation&gt; pPerf;
HRESULT hr = pContext-&gt;QueryInterface( __uuidof(pPerf), reinterpret_cast&lt;void**&gt;(&amp;pPerf) );
if ( FAILED( hr ) ) 
    return;
pPerf-&gt;BeginEvent( L”Now entering ocean rendering code” );
MyDrawOceanRoutine( );
pPerf-&gt;EndEvent( );
          </pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/255DE24B-3D6D-49D9-B6A8-D296AB99B4C9">ID3DUserDefinedAnnotation</a>
 

 

