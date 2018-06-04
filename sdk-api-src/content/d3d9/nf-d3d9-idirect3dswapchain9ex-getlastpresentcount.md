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

# IDirect3DSwapChain9Ex::GetLastPresentCount


## -description


Returns the number of times the swapchain has been processed.


## -parameters




### -param pLastPresentCount [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to a UINT to be filled with the number of times the <a href="https://msdn.microsoft.com/845c72ff-669d-44bf-8065-cff456418e8c">IDirect3DDevice9Ex::PresentEx</a> method has been called. The count will also be incremented by calling some other APIs such as <a href="https://msdn.microsoft.com/4cca59f4-07ae-42d2-9dc8-3ec90ad75f3b">IDirect3DDevice9::SetDialogBoxMode</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

S_OK the method was successful.




## -see-also




<a href="https://msdn.microsoft.com/b5af736b-f1d6-4db2-bd57-d88fca65b0a6">IDirect3DSwapChain9Ex</a>
 

 

