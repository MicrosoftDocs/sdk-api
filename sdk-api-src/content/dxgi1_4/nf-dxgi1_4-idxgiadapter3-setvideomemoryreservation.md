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

# IDXGIAdapter3::SetVideoMemoryReservation


## -description



          This method sends the minimum required physical memory for an application, to the OS.
        


## -parameters




### -param NodeIndex [in]

Type: <b>UINT</b>


            Specifies the device's physical adapter for which the video memory information is being set.
            For single-GPU operation, set this to zero.
            If there are multiple GPU nodes, set this to the index of the node (the device's physical adapter) for which the video memory information is being set.
            See <a href="https://msdn.microsoft.com/CC4C6594-D48F-40C1-93EE-9F98532BC038">Multi-Adapter</a>.
          


### -param MemorySegmentGroup [in]

Type: <b><a href="https://msdn.microsoft.com/2FE35513-040E-41BF-866E-A13679C4F322">DXGI_MEMORY_SEGMENT_GROUP</a></b>


            Specifies a DXGI_MEMORY_SEGMENT_GROUP that identifies the group as local or non-local.
          


### -param Reservation [in]

Type: <b>UINT64</b>


            Specifies a UINT64 that sets the minimum required physical memory, in bytes.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            Returns S_OK if successful; an error code otherwise.
            For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.
          




## -remarks




          Applications are encouraged to set a video reservation to denote the amount of physical memory they cannot go without.
          This value helps the OS quickly minimize the impact of large memory pressure situations.
        




## -see-also




<a href="https://msdn.microsoft.com/547840B4-4AAB-4049-8D79-BD34BA4D32CD">IDXGIAdapter3</a>
 

 

