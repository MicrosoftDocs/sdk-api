---
UID: NF:dxgi.IDXGIAdapter1.GetDesc1
title: IDXGIAdapter1::GetDesc1
author: windows-sdk-content
description: Gets a DXGI 1.1 description of an adapter (or video card).
old-location: direct3ddxgi\idxgiadapter1_getdesc1.htm
tech.root: direct3ddxgi
ms.assetid: 1eb051f8-4e64-41fe-8177-6aad47714cb9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDesc1, GetDesc1 method [DXGI], GetDesc1 method [DXGI],IDXGIAdapter1 interface, IDXGIAdapter1 interface [DXGI],GetDesc1 method, IDXGIAdapter1.GetDesc1, IDXGIAdapter1::GetDesc1, b985f570-96ae-e1c8-11c4-3485b12285bc, direct3ddxgi.idxgiadapter1_getdesc1, dxgi/IDXGIAdapter1::GetDesc1
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
 - IDXGIAdapter1.GetDesc1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIAdapter1::GetDesc1


## -description


Gets a DXGI 1.1 description of an adapter (or video card).


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/0ae3bdb1-b122-439a-8f62-c831a9dd87e2">DXGI_ADAPTER_DESC1</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/0ae3bdb1-b122-439a-8f62-c831a9dd87e2">DXGI_ADAPTER_DESC1</a> structure that describes the adapter.  
      This parameter must not be <b>NULL</b>. On <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a> 9 graphics hardware, <b>GetDesc1</b> returns zeros for the PCI ID in the <b>VendorId</b>, <b>DeviceId</b>, <b>SubSysId</b>, and <b>Revision</b> members of <b>DXGI_ADAPTER_DESC1</b> and “Software Adapter” for the description string in the <b>Description</b> member.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns E_INVALIDARG if the <i>pDesc</i> parameter is <b>NULL</b>.  
        




## -remarks



This method is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="http://go.microsoft.com/fwlink/p/?linkid=160189">KB 971644</a>) and Windows Server 2008 (<a href="http://go.microsoft.com/fwlink/p/?linkid=183689">KB 971512</a>).

Use the <b>GetDesc1</b> method to get a DXGI 1.1 description of an adapter.  To get a DXGI 1.0 description, use the <a href="https://msdn.microsoft.com/en-us/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a> method.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/003d5a10-e978-481f-8ca6-9e5ab69bfec0">IDXGIAdapter1</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174526(v=VS.85).aspx">IDXGIAdapter::GetDesc</a>
 

 

