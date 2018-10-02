---
UID: NF:dxgi.IDXGIFactory1.IsCurrent
title: IDXGIFactory1::IsCurrent
author: windows-sdk-content
description: Informs an application of the possible need to re-enumerate adapters.
old-location: direct3ddxgi\idxgifactory1_iscurrent.htm
tech.root: direct3ddxgi
ms.assetid: e1337b20-85c2-48e1-9205-aa729c0d0edc
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDXGIFactory1 interface [DXGI],IsCurrent method, IDXGIFactory1.IsCurrent, IDXGIFactory1::IsCurrent, IsCurrent, IsCurrent method [DXGI], IsCurrent method [DXGI],IDXGIFactory1 interface, a9f61d9d-ccf9-6f3c-a7a3-9545c2b59500, direct3ddxgi.idxgifactory1_iscurrent, dxgi/IDXGIFactory1::IsCurrent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DXGI.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIFactory1.IsCurrent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIFactory1::IsCurrent


## -description


Informs an application of the possible need to re-enumerate adapters.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>FALSE</b>, if a new adapter is becoming available or the current adapter is going away.
    <b>TRUE</b>, no adapter changes.

<b>IsCurrent</b> returns <b>FALSE</b> to inform the calling application to re-enumerate adapters.




## -remarks



This method is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="http://go.microsoft.com/fwlink/p/?linkid=160189">KB 971644</a>) and Windows Server 2008 (<a href="http://go.microsoft.com/fwlink/p/?linkid=183689">KB 971512</a>).




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/271f1877-25a7-4d32-9ffa-cb174b366b74">IDXGIFactory1</a>
 

 

