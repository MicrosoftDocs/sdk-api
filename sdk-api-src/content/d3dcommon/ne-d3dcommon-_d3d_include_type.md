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

# _D3D_INCLUDE_TYPE enumeration


## -description


Values that indicate the location of a shader #include file. 


## -enum-fields




### -field D3D_INCLUDE_LOCAL

The local directory.


### -field D3D_INCLUDE_SYSTEM

The system directory.


### -field D3D10_INCLUDE_LOCAL

The local directory.


### -field D3D10_INCLUDE_SYSTEM

The system directory.


### -field D3D_INCLUDE_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. 

Do not use this value.


## -remarks



You pass a <b>D3D_INCLUDE_TYPE</b>-typed value to the  <i>IncludeType</i> parameter in a call to the  <a href="https://msdn.microsoft.com/4d10c986-1cba-427c-ae90-f81b83be1b8b">ID3DInclude::Open</a> method to indicate the location of the #include file.




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>



<a href="https://msdn.microsoft.com/98f0b0dd-9ff8-4321-a9ea-2deabc9529f2">D3D_INCLUDE_TYPE</a>



<a href="https://msdn.microsoft.com/4d10c986-1cba-427c-ae90-f81b83be1b8b">ID3DInclude::Open</a>
 

 

