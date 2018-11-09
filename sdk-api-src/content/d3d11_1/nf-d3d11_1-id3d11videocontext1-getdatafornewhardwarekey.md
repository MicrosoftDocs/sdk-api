---
UID: NF:d3d11_1.ID3D11VideoContext1.GetDataForNewHardwareKey
title: ID3D11VideoContext1::GetDataForNewHardwareKey
author: windows-sdk-content
description: Allows the driver to return IHV specific information used when initializing the new hardware key.
old-location: mf\id3d11videocontext1_getdatafornewhardwarekey.htm
tech.root: medfound
ms.assetid: 4C02F80C-CF7A-4E66-9172-D55A31986ACD
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetDataForNewHardwareKey, GetDataForNewHardwareKey method [Media Foundation], GetDataForNewHardwareKey method [Media Foundation],ID3D11VideoContext1 interface, ID3D11VideoContext1 interface [Media Foundation],GetDataForNewHardwareKey method, ID3D11VideoContext1.GetDataForNewHardwareKey, ID3D11VideoContext1::GetDataForNewHardwareKey, d3d11_1/ID3D11VideoContext1::GetDataForNewHardwareKey, mf.id3d11videocontext1_getdatafornewhardwarekey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_1.h
api_name:
 - ID3D11VideoContext1.GetDataForNewHardwareKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext1::GetDataForNewHardwareKey


## -description


Allows the driver to return IHV specific information used when initializing the new hardware key.


## -parameters




### -param pCryptoSession [in]

Type: <b>ID3D11CryptoSession*</b>

A pointer to the ID3D11CryptoSession interface.  To get this pointer, call <a href="https://msdn.microsoft.com/en-us/library/Dd318827(v=VS.85).aspx">ID3D11VideoDevice1::CreateCryptoSession</a>.


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



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

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




<a href="https://msdn.microsoft.com/en-us/library/Dn894126(v=VS.85).aspx">ID3D11VideoContext1</a>
 

 

