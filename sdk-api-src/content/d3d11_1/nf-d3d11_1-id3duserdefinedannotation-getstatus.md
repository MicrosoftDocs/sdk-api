---
UID: NF:d3d11_1.ID3DUserDefinedAnnotation.GetStatus
title: ID3DUserDefinedAnnotation::GetStatus
author: windows-sdk-content
description: Determines whether the calling application is running under a Microsoft Direct3D profiling tool.
old-location: direct3d11\id3duserdefinedannotation_getstatus.htm
old-project: direct3d11
ms.assetid: 67C95617-3454-4457-AB3B-FD79C176E314
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: GetStatus, GetStatus method [Direct3D 11], GetStatus method [Direct3D 11],ID3DUserDefinedAnnotation interface, ID3DUserDefinedAnnotation interface [Direct3D 11],GetStatus method, ID3DUserDefinedAnnotation.GetStatus, ID3DUserDefinedAnnotation::GetStatus, d3d11_1/ID3DUserDefinedAnnotation::GetStatus, direct3d11.id3duserdefinedannotation_getstatus
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
-	ID3DUserDefinedAnnotation.GetStatus
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3DUserDefinedAnnotation::GetStatus


## -description


Determines whether the calling application is running under a Microsoft Direct3D profiling tool.


## -parameters






## -returns



The return value is nonzero if the calling application is running under a Direct3D profiling tool such as Visual Studio Ultimate 2012, and zero otherwise.




## -remarks



You can call <b>GetStatus</b> to determine whether your application is running under a Direct3D profiling tool before you make further calls to other methods of the <a href="https://msdn.microsoft.com/255DE24B-3D6D-49D9-B6A8-D296AB99B4C9">ID3DUserDefinedAnnotation</a> interface. For example, the <a href="https://msdn.microsoft.com/38FC7BFA-A01E-4537-88F1-836AE03C9A07">ID3DUserDefinedAnnotation::BeginEvent</a> and <a href="https://msdn.microsoft.com/5C478278-EC05-4214-80F9-808EADA76E41">ID3DUserDefinedAnnotation::EndEvent</a> methods have no effect if the calling application is not running under an enabled Direct3D profiling tool. Therefore, you do not need to call these methods unless your application is running under a Direct3D profiling tool.


#### Examples


          The following code shows how to use <b>GetStatus</b>.
          

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
#ifdef DEVELOPMENT_BUILD
    if ( pPerf-&gt;GetStatus() )
        m_MakeD3DAnnotationCalls = true;
#endif

…

   if ( m_ MakeD3DAnnotationCalls )
        pPerf-&gt;BeginEvent(L“Drawing Ocean”);
   MyDrawOceanRoutine();

          </pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/255DE24B-3D6D-49D9-B6A8-D296AB99B4C9">ID3DUserDefinedAnnotation</a>
 

 

