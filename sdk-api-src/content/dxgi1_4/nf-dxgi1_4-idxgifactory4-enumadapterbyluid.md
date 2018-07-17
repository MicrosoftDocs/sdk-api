---
UID: NF:dxgi1_4.IDXGIFactory4.EnumAdapterByLuid
title: IDXGIFactory4::EnumAdapterByLuid
author: windows-sdk-content
description: Outputs the IDXGIAdapter for the specified LUID.
old-location: direct3ddxgi\idxgifactory4_enumadapterbyluid.htm
old-project: direct3ddxgi
ms.assetid: AC800F32-2922-45BA-A6D3-D3E45113B9A7
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: EnumAdapterByLuid, EnumAdapterByLuid method [DXGI], EnumAdapterByLuid method [DXGI],IDXGIFactory4 interface, IDXGIFactory4 interface [DXGI],EnumAdapterByLuid method, IDXGIFactory4.EnumAdapterByLuid, IDXGIFactory4::EnumAdapterByLuid, direct3ddxgi.idxgifactory4_enumadapterbyluid, dxgi1_4/IDXGIFactory4::EnumAdapterByLuid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_4.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: DXGI_SWAP_CHAIN_COLOR_SPACE_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIFactory4.EnumAdapterByLuid
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIFactory4::EnumAdapterByLuid


## -description



          Outputs the <a href="https://msdn.microsoft.com/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a> for the specified LUID.
        


## -parameters




### -param AdapterLuid [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a></b>


            A unique value that identifies the adapter.
            See <a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> for a definition of the structure.
            <b>LUID</b> is defined in dxgi.h.
          


### -param riid [in]

Type: <b>REFIID</b>


            The globally unique identifier (GUID) of the <a href="https://msdn.microsoft.com/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a> object referenced by the <i>ppvAdapter</i> parameter.
          


### -param ppvAdapter [out]

Type: <b>void**</b>


            The address of an <a href="https://msdn.microsoft.com/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a> interface pointer to the adapter.
            This parameter must not be NULL.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>


            Returns S_OK if successful; an error code otherwise.
            For a list of error codes, see <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.
            See also Direct3D 12 Return Codes.
          




## -remarks




          For Direct3D 12, it's no longer possible to backtrack from a device to the <a href="https://msdn.microsoft.com/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a> that was used to create it.
          <b>IDXGIFactory4::EnumAdapterByLuid</b>
          enables an app to retrieve information about the adapter where a D3D12 device was created.
          <b>IDXGIFactory4::EnumAdapterByLuid</b> is designed to be paired with <a href="https://msdn.microsoft.com/006E72E0-AE09-4834-9ACB-D48698050BF2">ID3D12Device::GetAdapterLuid</a>.
          For more information, see <a href="https://msdn.microsoft.com/DEA901EA-B0F9-41D9-802C-ED1D6A7888E0">DXGI 1.4 Improvements</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/248CF7CF-BC7D-430F-9EA1-638A42AAC021">IDXGIFactory4</a>
 

 

