---
UID: NF:d3d11.ID3D11ClassInstance.GetTypeName
title: ID3D11ClassInstance::GetTypeName method
author: windows-driver-content
description: Gets the type of the current HLSL class.
old-location: direct3d11\id3d11classinstance_gettypename.htm
old-project: direct3d11
ms.assetid: a46699b5-2250-442a-85ab-37eeb419ac72
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 37b4ce30-bd10-e500-268b-fcbfc22464f2, GetTypeName method [Direct3D 11], GetTypeName method [Direct3D 11], ID3D11ClassInstance interface, GetTypeName,ID3D11ClassInstance.GetTypeName, ID3D11ClassInstance, ID3D11ClassInstance interface [Direct3D 11], GetTypeName method, ID3D11ClassInstance::GetTypeName, d3d11/ID3D11ClassInstance::GetTypeName, direct3d11.id3d11classinstance_gettypename
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11.lib
-	d3d11.dll
api_name:
-	ID3D11ClassInstance.GetTypeName
product: Windows
targetos: Windows
req.lib: D3d11.lib
req.dll: 
req.irql: 
---

# ID3D11ClassInstance::GetTypeName method


## -description


Gets the type of the current HLSL class.


## -parameters




### -param pTypeName [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPSTR</a></b>

Type of the current HLSL class.


### -param pBufferLength [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a>*</b>


            The length of the <i>pTypeName</i> parameter.
          


## -returns



This method does not return a value.




## -remarks



GetTypeName will return a valid name only for instances acquired using <a href="https://msdn.microsoft.com/055f1670-0643-4a0a-8411-ac8a62e98826">ID3D11ClassLinkage::GetClassInstance</a>.
        


          For more information about using the <a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a> interface, see <a href="https://msdn.microsoft.com/2f5f7852-0f0a-4fad-a412-9a0d634c73b6">Dynamic Linking</a>.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a>
 

 

