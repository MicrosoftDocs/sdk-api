---
UID: NF:dxgi1_4.IDXGIAdapter3.QueryVideoMemoryInfo
title: IDXGIAdapter3::QueryVideoMemoryInfo
author: windows-sdk-content
description: This method informs the process of the current budget and process usage.
old-location: direct3ddxgi\idxgiadapter3_queryvideomemoryinfo.htm
tech.root: direct3ddxgi
ms.assetid: A2F95FE5-CF8D-4F17-8CC8-62AAA40B71FC
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDXGIAdapter3 interface [DXGI],QueryVideoMemoryInfo method, IDXGIAdapter3.QueryVideoMemoryInfo, IDXGIAdapter3::QueryVideoMemoryInfo, QueryVideoMemoryInfo, QueryVideoMemoryInfo method [DXGI], QueryVideoMemoryInfo method [DXGI],IDXGIAdapter3 interface, direct3ddxgi.idxgiadapter3_queryvideomemoryinfo, dxgi1_4/IDXGIAdapter3::QueryVideoMemoryInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_4.h
req.include-header: DXGI1_3.h
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
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIAdapter3.QueryVideoMemoryInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxgi1_4.h
: 
- IDXGIAdapter3.QueryVideoMemoryInfo
: 
---

# IDXGIAdapter3::QueryVideoMemoryInfo


## -description


This method informs the process of the current budget and process usage.
        


## -parameters




### -param NodeIndex [in]

Type: <b>UINT</b>

Specifies the device's physical adapter for which the video memory information is queried.
            For single-GPU operation, set this to zero.
            If there are multiple GPU nodes, set this to the index of the node (the device's physical adapter) for which the video memory information is queried.
            See <a href="https://msdn.microsoft.com/CC4C6594-D48F-40C1-93EE-9F98532BC038">Multi-Adapter</a>.
          


### -param MemorySegmentGroup [in]

Type: <b><a href="https://msdn.microsoft.com/2FE35513-040E-41BF-866E-A13679C4F322">DXGI_MEMORY_SEGMENT_GROUP</a></b>

Specifies a DXGI_MEMORY_SEGMENT_GROUP that identifies the group as local or non-local.
          


### -param pVideoMemoryInfo [out]

Type: <b><a href="https://msdn.microsoft.com/E710F3A9-CB12-43B0-B56C-789350BCAE59">DXGI_QUERY_VIDEO_MEMORY_INFO</a>*</b>

Fills in a DXGI_QUERY_VIDEO_MEMORY_INFO structure with the current values.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns S_OK if successful; an error code otherwise.
            For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.
          




## -remarks



Applications must explicitly manage their usage of physical memory explicitly and keep usage within the budget assigned to the application process.
          Processes that cannot kept their usage within their assigned budgets will likely experience stuttering, as they are intermittently frozen and paged-out to allow other processes to run.
        




## -see-also




<a href="https://msdn.microsoft.com/547840B4-4AAB-4049-8D79-BD34BA4D32CD">IDXGIAdapter3</a>
 

 

