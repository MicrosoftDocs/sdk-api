---
UID: NF:d3d11_1.ID3D11VideoContext1.CheckCryptoSessionStatus
title: ID3D11VideoContext1::CheckCryptoSessionStatus
author: windows-sdk-content
description: Checks the status of a crypto session.
old-location: mf\id3d11videocontext1_checkcryptosessionstatus.htm
tech.root: medfound
ms.assetid: 07126C45-2771-432C-9644-FD4099B8D26D
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CheckCryptoSessionStatus, CheckCryptoSessionStatus method [Media Foundation], CheckCryptoSessionStatus method [Media Foundation],ID3D11VideoContext1 interface, ID3D11VideoContext1 interface [Media Foundation],CheckCryptoSessionStatus method, ID3D11VideoContext1.CheckCryptoSessionStatus, ID3D11VideoContext1::CheckCryptoSessionStatus, d3d11_1/ID3D11VideoContext1::CheckCryptoSessionStatus, mf.id3d11videocontext1_checkcryptosessionstatus
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
 - ID3D11VideoContext1.CheckCryptoSessionStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext1::CheckCryptoSessionStatus


## -description


Checks the status of a crypto session.


## -parameters




### -param pCryptoSession [in]

Type: <b>ID3D11CryptoSession*</b>

Specifies a <a href="https://msdn.microsoft.com/en-us/library/Hh447691(v=VS.85).aspx">ID3D11CryptoSession</a> for which status is checked.


### -param pStatus [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn894114(v=VS.85).aspx">D3D11_CRYPTO_SESSION_STATUS</a>*</b>

A D3D11_CRYPTO_SESSION_STATUS that is populated with the crypto session status upon completion.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following error codes.

<table>
<tr>
<td>S_OK</td>
<td>The operation completed successfully.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed or this function was called using an invalid calling pattern.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>There is insufficient memory to complete the operation.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn894126(v=VS.85).aspx">ID3D11VideoContext1</a>
 

 

