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
 

 

