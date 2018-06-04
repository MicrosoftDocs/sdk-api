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

# IDXGIFactory4::EnumWarpAdapter


## -description



          Provides an adapter which can be provided to D3D12CreateDevice to use the WARP renderer.
        


## -parameters




### -param riid [in]

Type: <b>REFIID</b>


            The globally unique identifier (GUID) of the <a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a> object referenced by the <i>ppvAdapter</i> parameter.
          


### -param ppvAdapter [out]

Type: <b>void**</b>


            The address of an <a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a> interface pointer to the adapter.
            This parameter must not be NULL.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            Returns S_OK if successful; an error code otherwise.
            For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.
            See also Direct3D 12 Return Codes.
          




## -remarks




          For more information, see <a href="https://msdn.microsoft.com/DEA901EA-B0F9-41D9-802C-ED1D6A7888E0">DXGI 1.4 Improvements</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/248CF7CF-BC7D-430F-9EA1-638A42AAC021">IDXGIFactory4</a>
 

 

