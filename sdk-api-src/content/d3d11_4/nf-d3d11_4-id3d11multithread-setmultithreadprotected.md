---
UID: NF:d3d11_4.ID3D11Multithread.SetMultithreadProtected
title: ID3D11Multithread::SetMultithreadProtected
author: windows-sdk-content
description: Turns multithread protection on or off.
old-location: direct3d11\id3d11multithread_setmultithreadprotected.htm
old-project: direct3d11
ms.assetid: E8BF9A25-CCEA-44F3-AE7C-376E5B672079
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11Multithread interface [Direct3D 11],SetMultithreadProtected method, ID3D11Multithread.SetMultithreadProtected, ID3D11Multithread::SetMultithreadProtected, SetMultithreadProtected, SetMultithreadProtected method [Direct3D 11], SetMultithreadProtected method [Direct3D 11],ID3D11Multithread interface, d3d11_4/ID3D11Multithread::SetMultithreadProtected, direct3d11.id3d11multithread_setmultithreadprotected
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11_4.h
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
tech.root: 
req.typenames: D3D11_UNORDERED_ACCESS_VIEW_DESC1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_4.dll
api_name:
 - ID3D11Multithread.SetMultithreadProtected
product: Windows
targetos: Windows
req.lib: D3d11_4.lib
req.dll: D3d11_4.dll
req.irql: 
---

# ID3D11Multithread::SetMultithreadProtected


## -description


Turns multithread protection on or off.


## -parameters




### -param bMTProtect [in]

Type: <b>BOOL</b>

Set to true to turn multithread protection on, false to turn it off.


## -returns



Type: <b>BOOL</b>

True if multithread protection was already turned on prior to calling this method, false otherwise. 




## -see-also




<a href="https://msdn.microsoft.com/1BCB0021-9C92-425D-97C1-6EDB1D2127A8">GetMultithreadProtected</a>



<a href="https://msdn.microsoft.com/1A07694E-7D61-4A59-82E3-048F04C8D57A">ID3D11Multithread</a>
 

 

