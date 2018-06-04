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

# ID3DInclude::Close


## -description


A user-implemented method for closing a shader #include file.


## -parameters




### -param pData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCVOID</a></b>


            Pointer to the buffer that contains the include directives. This is the pointer that was returned by the corresponding <a href="https://msdn.microsoft.com/4d10c986-1cba-427c-ae90-f81b83be1b8b">ID3DInclude::Open</a> call.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


                The user-implemented <b>Close</b> method should return S_OK. If <b>Close</b> fails when it closes the #include file, the application programming interface (API) that caused <b>Close</b> to be called fails. This failure can occur in one of the following situations:
              

<ul>
<li>
                The high-level shader language (HLSL) shader fails one of the <b>D3D10CompileShader***</b> functions.
              </li>
<li>
                The effect fails one of the <b>D3D10CreateEffect***</b> functions.
              </li>
</ul>



## -remarks




          If <a href="https://msdn.microsoft.com/4d10c986-1cba-427c-ae90-f81b83be1b8b">ID3DInclude::Open</a> was successful, <b>Close</b> is guaranteed to be called before the API using the <a href="https://msdn.microsoft.com/2020ce65-3a6e-4a9f-9e97-b94e3c75f4f5">ID3DInclude</a> interface returns.
        




## -see-also




<a href="https://msdn.microsoft.com/2020ce65-3a6e-4a9f-9e97-b94e3c75f4f5">ID3DInclude</a>



<a href="https://msdn.microsoft.com/4d10c986-1cba-427c-ae90-f81b83be1b8b">ID3DInclude::Open</a>
 

 

