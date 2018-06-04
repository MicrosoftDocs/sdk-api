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

# ID3D12Object::SetName


## -description



          Associates a name with the device object.
          This name is for use in debug diagnostics and tools.
        


## -parameters




### -param Name [in]

Type: <b>LPCWSTR</b>


            A <b>NULL</b>-terminated <b>UNICODE</b> string that contains the name to associate with the device object.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks




        This method takes UNICODE names.
        The older Direct3D 11 debug object naming system through
        <a href="https://msdn.microsoft.com/1B3E8202-7CB3-4D9F-A1AE-70E66652773C">ID3D12Object::SetPrivateData</a>
        with <b>WKPDID_D3DDebugObjectName</b> used ASCII.
       




## -see-also




<a href="https://msdn.microsoft.com/B2288866-E95F-46B8-A7A1-19888F029C03">Direct3D 12 Programming Environment Setup</a>



<a href="https://msdn.microsoft.com/D2B2BC74-E89D-4D3A-8808-6E4A94992769">ID3D12Object</a>
 

 

