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

# IDXGISurface::Map


## -description


Get a pointer to the data contained in the surface, and deny GPU access to the surface.


## -parameters




### -param pLockedRect [out]

Type: <b><a href="https://msdn.microsoft.com/9f5e33d9-3b82-4b5e-8ddc-aacd581b829b">DXGI_MAPPED_RECT</a>*</b>

A pointer to the surface data (see <a href="https://msdn.microsoft.com/9f5e33d9-3b82-4b5e-8ddc-aacd581b829b">DXGI_MAPPED_RECT</a>).


### -param MapFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

CPU read-write flags. These flags can be combined with a logical OR.



<ul>
<li>DXGI_MAP_READ - Allow CPU read access.</li>
<li>DXGI_MAP_WRITE - Allow CPU write access.</li>
<li>DXGI_MAP_DISCARD - Discard the previous contents of a resource when it is mapped.</li>
</ul>

## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.




## -remarks



Use <b>IDXGISurface::Map</b> to access a surface from the CPU. To release a mapped surface (and allow GPU access) call <a href="https://msdn.microsoft.com/cf685888-422d-4559-9b0c-7d1335d22906">IDXGISurface::Unmap</a>.




## -see-also




<a href="https://msdn.microsoft.com/9210b966-9e9a-4cd1-ba70-6f1a9fda9d80">IDXGISurface</a>
 

 

