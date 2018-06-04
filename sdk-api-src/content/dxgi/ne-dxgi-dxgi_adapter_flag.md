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

# DXGI_ADAPTER_FLAG enumeration


## -description


Identifies the type of DXGI adapter.


## -enum-fields




### -field DXGI_ADAPTER_FLAG_NONE

Specifies no flags.


### -field DXGI_ADAPTER_FLAG_REMOTE

Value always set to 0. This flag is reserved.


### -field DXGI_ADAPTER_FLAG_SOFTWARE

Specifies a software adapter. For more info about this flag, see <a href="d3d10_graphics_programming_guide_dxgi.htm">new info in Windows 8 about enumerating adapters</a>.

<b>Direct3D 11:  </b>This enumeration value is supported starting with Windows 8.


### -field DXGI_ADAPTER_FLAG_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile 
          to a size other than 32 bits. This value is not used.


## -remarks



The <b>DXGI_ADAPTER_FLAG</b> enumerated type is used by the <b>Flags</b> member of the <a href="https://msdn.microsoft.com/0ae3bdb1-b122-439a-8f62-c831a9dd87e2">DXGI_ADAPTER_DESC1</a> or <a href="https://msdn.microsoft.com/AE34913A-84D8-49DB-A736-15AECA9989F9">DXGI_ADAPTER_DESC2</a> structure to 
      identify the type of DXGI adapter.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

