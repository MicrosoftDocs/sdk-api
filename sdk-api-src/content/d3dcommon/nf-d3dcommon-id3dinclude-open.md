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

# ID3DInclude::Open


## -description


A user-implemented method for opening and reading the contents of a shader #include file.


## -parameters




### -param IncludeType

Type: <b><a href="https://msdn.microsoft.com/98f0b0dd-9ff8-4321-a9ea-2deabc9529f2">D3D_INCLUDE_TYPE</a></b>


            A <a href="https://msdn.microsoft.com/98f0b0dd-9ff8-4321-a9ea-2deabc9529f2">D3D_INCLUDE_TYPE</a>-typed value that indicates the location of the #include file.
          


### -param pFileName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

Name of the #include file.


### -param pParentData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCVOID</a></b>


            Pointer to the container that includes the #include file. The compiler might pass NULL in <i>pParentData</i>. For more information, see the "Searching for Include Files" section in <a href="https://msdn.microsoft.com/7624d55e-6466-4156-8f31-30f0d25a2883">Compile an Effect (Direct3D 11)</a>.
          


### -param ppData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCVOID</a>*</b>


            Pointer to the buffer  that contains the include directives. This pointer remains valid until you call<a href="https://msdn.microsoft.com/d4513e15-dfe7-4919-a278-d386f25e65e5">ID3DInclude::Close</a>.
          


### -param pBytes

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>


            Pointer to the number of bytes that <b>Open</b> returns in <i>ppData</i>.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


                The user-implemented method must return S_OK. If <b>Open</b> fails when it reads the #include file, the application programming interface (API) that caused <b>Open</b> to be called fails. This failure can occur in one of the following situations:
              

<ul>
<li>
                The high-level shader language (HLSL) shader fails one of the <b>D3D10CompileShader***</b> functions.
              </li>
<li>
                The effect fails one of the <b>D3D10CreateEffect***</b> functions.
              </li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/2020ce65-3a6e-4a9f-9e97-b94e3c75f4f5">ID3DInclude</a>



<a href="https://msdn.microsoft.com/d4513e15-dfe7-4919-a278-d386f25e65e5">ID3DInclude::Close</a>
 

 

