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

# ID3D11VideoContext1::GetDataForNewHardwareKey


## -description


Allows the driver to return IHV specific information used when initializing the new hardware key.


## -parameters




### -param pCryptoSession [in]

Type: <b>ID3D11CryptoSession*</b>

A pointer to the ID3D11CryptoSession interface.  To get this pointer, call <a href="https://msdn.microsoft.com/1c0e3aa4-94d5-4398-a6c0-5466a437162d">ID3D11VideoDevice1::CreateCryptoSession</a>.


### -param PrivateInputSize [in]

Type: <b>UINT</b>

The size of the memory referenced by the <i>pPrivateInputData</i> parameter.


### -param pPrivatInputData [in]

Type: <b>const void*</b>

The private input data. The contents of this parameter is defined by the implementation of the secure execution environment. It may contain data about the license or about the stream properties.


### -param pPrivateOutputData [out]

Type: <b>UINT64*</b>

A pointer to the private output data. The return data is defined by the implementation of the secure execution environment. It may contain graphics-specific data to be associated with the underlying hardware key.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following error codes.

<table>
<tr>
<td>S_OK</td>
<td>The operation completed successfully.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>There is insufficient memory to complete the operation.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/64D12F68-C2AA-4C1D-9608-5F97CF7AD430">ID3D11VideoContext1</a>
 

 

