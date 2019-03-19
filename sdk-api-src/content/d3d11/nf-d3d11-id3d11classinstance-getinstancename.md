---
UID: NF:d3d11.ID3D11ClassInstance.GetInstanceName
title: ID3D11ClassInstance::GetInstanceName (d3d11.h)
author: windows-sdk-content
description: Gets the instance name of the current HLSL class.
old-location: direct3d11\id3d11classinstance_getinstancename.htm
tech.root: direct3d11
ms.assetid: 9e9c3410-6421-4300-b3a6-de4840a81117
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 52fdee2c-7566-954c-edad-a7d91948caac, GetInstanceName, GetInstanceName method [Direct3D 11], GetInstanceName method [Direct3D 11],ID3D11ClassInstance interface, ID3D11ClassInstance interface [Direct3D 11],GetInstanceName method, ID3D11ClassInstance.GetInstanceName, ID3D11ClassInstance::GetInstanceName, d3d11/ID3D11ClassInstance::GetInstanceName, direct3d11.id3d11classinstance_getinstancename
ms.topic: method
req.header: d3d11.h
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
req.lib: D3d11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11ClassInstance.GetInstanceName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ClassInstance::GetInstanceName


## -description


Gets the instance name of the current HLSL class.


## -parameters




### -param pInstanceName [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPSTR</a></b>

The instance name of the current HLSL class.


### -param pBufferLength [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a>*</b>

The length of the <i>pInstanceName</i> parameter.
          


## -returns



This method does not return a value.




## -remarks



GetInstanceName will return a valid name only for instances acquired using 
          <a href="https://msdn.microsoft.com/055f1670-0643-4a0a-8411-ac8a62e98826">ID3D11ClassLinkage::GetClassInstance</a>.
        

For more information about using the <a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a> interface, see 
          <a href="https://msdn.microsoft.com/2f5f7852-0f0a-4fad-a412-9a0d634c73b6">Dynamic Linking</a>.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a>
 

 

