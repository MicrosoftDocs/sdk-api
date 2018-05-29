---
UID: NF:d3d11_1.ID3DUserDefinedAnnotation.BeginEvent
title: ID3DUserDefinedAnnotation::BeginEvent
author: windows-sdk-content
description: Marks the beginning of a section of event code.
old-location: direct3d11\id3duserdefinedannotation_beginevent.htm
old-project: direct3d11
ms.assetid: 38FC7BFA-A01E-4537-88F1-836AE03C9A07
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: BeginEvent, BeginEvent method [Direct3D 11], BeginEvent method [Direct3D 11],ID3DUserDefinedAnnotation interface, ID3DUserDefinedAnnotation interface [Direct3D 11],BeginEvent method, ID3DUserDefinedAnnotation.BeginEvent, ID3DUserDefinedAnnotation::BeginEvent, d3d11_1/ID3DUserDefinedAnnotation::BeginEvent, direct3d11.id3duserdefinedannotation_beginevent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3DUserDefinedAnnotation.BeginEvent
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
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
 

 

