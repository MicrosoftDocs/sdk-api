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

# D3D10CreateEffectPoolFromMemory function


## -description


Create an effect pool (or shared memory location), to enable sharing variables between effects.


## -parameters




### -param pData [in]

Type: <b>void*</b>

A pointer to a compiled effect.


### -param DataLength [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Length of <i>pData</i>.


### -param FXFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Effect <a href="https://msdn.microsoft.com/434bcff8-47ea-480d-bc0b-44d3ed1f8cce">compile options</a>.


### -param pDevice [in]

Type: <b><a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>*</b>

A pointer to the device (see <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>).


### -param ppEffectPool [out]

Type: <b><a href="https://msdn.microsoft.com/e64c9285-f4ee-4bed-a57d-8ccc3e6b3ba3">ID3D10EffectPool</a>**</b>

A pointer to the <a href="https://msdn.microsoft.com/e64c9285-f4ee-4bed-a57d-8ccc3e6b3ba3">ID3D10EffectPool Interface</a> that contains the effect pool.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



A pool is a shared location in memory. Effect variables that are located in a pool can be updated once, and the effect system will take care of updating each effect that uses that variable. To pool an effect variable, tell the effect to locate the variable in a pool when the effect is created, using a helper function such as <a href="https://msdn.microsoft.com/1418857e-bda1-4ffb-bbb9-dfa3709313b1">D3DX10CreateEffectFromFile</a>.

For help compiling an effect, see <a href="https://msdn.microsoft.com/b8d8a0b7-b520-44e4-8691-6eb46202c092">Compile an Effect (Direct3D 10)</a>.




## -see-also




<a href="https://msdn.microsoft.com/b76643f0-387f-49c6-80e5-4d7b406b4db7">Effect Functions (Direct3D 10)</a>
 

 

