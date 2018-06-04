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

# D3D10CreateStateBlock function


## -description


Create a state block.


## -parameters




### -param pDevice [in]

Type: <b><a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>*</b>

The device for which the state block will be created.


### -param pStateBlockMask [in]

Type: <b><a href="https://msdn.microsoft.com/3188002c-a49f-4991-8fd5-75b31de8b790">D3D10_STATE_BLOCK_MASK</a>*</b>

Indicates which parts of the device state will be captured when calling <a href="https://msdn.microsoft.com/ea55f168-dbb0-40de-908f-e8a4418894ae">ID3D10StateBlock::Capture</a> and reapplied when calling <a href="https://msdn.microsoft.com/4b5351ef-b2cd-4c80-a1ee-6e2b25d007b8">ID3D10StateBlock::Apply</a>. See remarks.


### -param ppStateBlock [out]

Type: <b><a href="https://msdn.microsoft.com/3705e8e6-f25f-4943-8c41-09fa6de02932">ID3D10StateBlock</a>**</b>

Address of a pointer to the buffer created (see <a href="https://msdn.microsoft.com/3705e8e6-f25f-4943-8c41-09fa6de02932">ID3D10StateBlock Interface</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



A state block is a collection of device state, and is used for saving and restoring device state. Use a state-block mask to enable subsets of state for saving and restoring.

The <a href="https://msdn.microsoft.com/3188002c-a49f-4991-8fd5-75b31de8b790">D3D10_STATE_BLOCK_MASK</a> structure can be filled manually or by using any of the D3D10StateBlockMaskXXX APIs. A state block mask can also be obtained by calling <a href="https://msdn.microsoft.com/c881dc2d-8e02-49b0-b539-bd0b1e767110">ID3D10EffectTechnique::ComputeStateBlockMask</a> or <a href="https://msdn.microsoft.com/ab4ad7b6-ad6a-44b5-bb07-42b7b92b3f1b">ID3D10EffectPass::ComputeStateBlockMask</a>.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

In Direct3D 10, a state block object does not contain any valid information about the state of the device until <a href="https://msdn.microsoft.com/ea55f168-dbb0-40de-908f-e8a4418894ae">ID3D10StateBlock::Capture</a> is called. In Direct3D 9, state is saved in a state block object, when it is created.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/012577cd-970e-43bc-996e-3be7c2283b60">Core Functions</a>



<a href="https://msdn.microsoft.com/b76643f0-387f-49c6-80e5-4d7b406b4db7">Effect Functions</a>
 

 

