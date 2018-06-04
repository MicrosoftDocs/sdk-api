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

# IDirect3DQuery9::Issue


## -description


Issue a query.


## -parameters




### -param dwIssueFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Query flags specify the type of state change for the query. See <a href="https://msdn.microsoft.com/21b8a2b0-d18f-4412-b655-3a913b7312ee">D3DISSUE_BEGIN</a> and <a href="https://msdn.microsoft.com/9ced932a-5d98-4bf8-aa11-06560f53546d">D3DISSUE_END</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



A signaled query means the query has completed, the data is available, and <a href="https://msdn.microsoft.com/5363b5a4-6ac1-4f4e-8d64-949968d2a08a">IDirect3DQuery9::GetData</a> will return S_OK. 




## -see-also




<a href="https://msdn.microsoft.com/7f25d64e-ece6-4544-ada0-5cc3d34b88e6">IDirect3DQuery9</a>
 

 

