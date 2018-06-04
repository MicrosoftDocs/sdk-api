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

# ID3D12Device::GetAdapterLuid


## -description



          Gets a locally unique identifier for the current device (adapter).
        


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a></b>


            The locally unique identifier for the adapter.
          




## -remarks




          This method returns a unique identifier for the adapter that is specific to the adapter hardware.
          Applications can use this identifier to define robust mappings across various APIs (Direct3D 12, DXGI).
        


          A locally unique identifier (LUID) is a 64-bit value that is guaranteed to be unique only on the system on which it was generated.
          The uniqueness of a locally unique identifier (LUID) is guaranteed only until the system is restarted.
        




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

