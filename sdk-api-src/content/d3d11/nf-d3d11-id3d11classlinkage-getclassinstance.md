---
UID: NF:d3d11.ID3D11ClassLinkage.GetClassInstance
title: ID3D11ClassLinkage::GetClassInstance
author: windows-sdk-content
description: Gets the class-instance object that represents the specified HLSL class.
old-location: direct3d11\id3d11classlinkage_getclassinstance.htm
old-project: direct3d11
ms.assetid: 055f1670-0643-4a0a-8411-ac8a62e98826
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 45d18e06-7ca3-6ff7-a95b-a56150c07b87, GetClassInstance, GetClassInstance method [Direct3D 11], GetClassInstance method [Direct3D 11],ID3D11ClassLinkage interface, ID3D11ClassLinkage interface [Direct3D 11],GetClassInstance method, ID3D11ClassLinkage.GetClassInstance, ID3D11ClassLinkage::GetClassInstance, d3d11/ID3D11ClassLinkage::GetClassInstance, direct3d11.id3d11classlinkage_getclassinstance
ms.prod: windows
ms.technology: windows-sdk
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
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11ClassLinkage.GetClassInstance
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11ClassLinkage::GetClassInstance


## -description


Gets the class-instance object that represents the specified HLSL class.


## -parameters




### -param pClassInstanceName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of a class for which to get the class instance.


### -param InstanceIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the class instance.


### -param ppInstance [out]

Type: <b><a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a>**</b>


            The address of a pointer to an <a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a> interface to initialize.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            Returns S_OK if successful; otherwise, returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.
          




## -remarks




          For more information about using the <a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a> interface, see
          <a href="https://msdn.microsoft.com/2f5f7852-0f0a-4fad-a412-9a0d634c73b6">Dynamic Linking</a>.
        


          A class instance must have at least 1 data member in order to be available for the runtime to use with
          <b>ID3D11ClassLinkage::GetClassInstance</b>.
          Any instance with no members will be optimized out of a compiled shader blob as a zero-sized object.
          If you have a class with no data members, use
          <a href="https://msdn.microsoft.com/26e5b1c7-d7b7-413b-a072-33f8f5dd5d3f">ID3D11ClassLinkage::CreateClassInstance</a> instead.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/70d006d2-5c47-4e8a-9a14-b5475d88ac32">ID3D11ClassInstance</a>



<a href="https://msdn.microsoft.com/eac03911-d881-4304-9598-912321ac0b0c">ID3D11ClassLinkage</a>
 

 

