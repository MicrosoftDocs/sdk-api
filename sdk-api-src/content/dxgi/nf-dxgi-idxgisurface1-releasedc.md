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

# IDXGISurface1::ReleaseDC


## -description


Releases the GDI device context (DC) that is associated with the current surface and allows you to use Direct3D to render.


## -parameters




### -param pDirtyRect [in, optional]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <b>RECT</b> structure that identifies the dirty region of the surface.  
          A dirty region is any part of the surface that you used for GDI rendering and that you want to preserve. 
          This area is used as a performance hint to graphics subsystem in certain scenarios. 
          Do not use this parameter to restrict rendering to the specified rectangular region. 
          If you pass in <b>NULL</b>, <b>ReleaseDC</b> considers the whole surface as dirty. 
          Otherwise, <b>ReleaseDC</b> uses the area specified by the RECT as a performance hint to indicate what areas have been manipulated by GDI rendering.

You can pass a pointer to an empty <b>RECT</b> structure (a rectangle with no position or area) if you didn't change any content.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="http://go.microsoft.com/fwlink/p/?linkid=160189">KB 971644</a>) and Windows Server 2008 (<a href="http://go.microsoft.com/fwlink/p/?linkid=183689">KB 971512</a>).

Use the <b>ReleaseDC</b> method to release the DC and indicate that your application finished all GDI rendering to this surface.  
      You must call the <b>ReleaseDC</b> method before you can use Direct3D to perform additional rendering.

Prior to resizing buffers you must release all outstanding DCs.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/99ece4f3-1bad-46b8-94a9-6ef559864b1c">IDXGISurface1</a>
 

 

