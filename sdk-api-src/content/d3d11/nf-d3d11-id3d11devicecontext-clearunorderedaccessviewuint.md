---
UID: NF:d3d11.ID3D11DeviceContext.ClearUnorderedAccessViewUint
title: ID3D11DeviceContext::ClearUnorderedAccessViewUint method
author: windows-driver-content
description: Clears an unordered access resource with bit-precise values.
old-location: direct3d11\id3d11devicecontext_clearunorderedaccessviewuint.htm
old-project: direct3d11
ms.assetid: 73e70330-63cb-4ba6-b6e5-fc9707fb9f31
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: 6de62b79-ec47-d4cc-7834-5acc4c87fa8d, ClearUnorderedAccessViewUint method [Direct3D 11], ClearUnorderedAccessViewUint method [Direct3D 11], ID3D11DeviceContext interface, ClearUnorderedAccessViewUint,ID3D11DeviceContext.ClearUnorderedAccessViewUint, ID3D11DeviceContext, ID3D11DeviceContext interface [Direct3D 11], ClearUnorderedAccessViewUint method, ID3D11DeviceContext::ClearUnorderedAccessViewUint, d3d11/ID3D11DeviceContext::ClearUnorderedAccessViewUint, direct3d11.id3d11devicecontext_clearunorderedaccessviewuint
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
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11DeviceContext.ClearUnorderedAccessViewUint
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::ClearUnorderedAccessViewUint method


## -description


Clears an <a href="https://msdn.microsoft.com/597cc12f-dd0e-4603-b670-3f584f25e192">unordered access</a> resource with bit-precise values.


## -parameters




### -param pUnorderedAccessView [in]

Type: <b><a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>*</b>

The <a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a> to clear.


### -param Values [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>[4]</b>

Values to copy to corresponding channels, see remarks.


## -returns



Returns nothing.




## -remarks



This API copies the lower n<sub>i</sub> bits from each array element i to the corresponding channel, where n<sub>i</sub> is the number of bits in 
      the ith channel of the resource format (for example, R8G8B8_FLOAT has 8 bits for the first 3 channels). This works on any UAV with no format conversion. 
      For a raw or structured buffer view, only the first array element value is used.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

