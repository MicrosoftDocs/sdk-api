---
UID: NF:d3d11_2.ID3D11DeviceContext2.SetMarkerInt
title: ID3D11DeviceContext2::SetMarkerInt
author: windows-sdk-content
description: Allows applications to annotate graphics commands.
old-location: direct3d11\id3d11devicecontext2_setmarkerint.htm
tech.root: direct3d11
ms.assetid: bb814f16-ca58-46ad-88eb-1c67b17d0c86
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11DeviceContext2 interface [Direct3D 11],SetMarkerInt method, ID3D11DeviceContext2.SetMarkerInt, ID3D11DeviceContext2::SetMarkerInt, SetMarkerInt, SetMarkerInt method [Direct3D 11], SetMarkerInt method [Direct3D 11],ID3D11DeviceContext2 interface, d3d11_2/ID3D11DeviceContext2::SetMarkerInt, direct3d11.id3d11devicecontext2_setmarkerint
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: D3d11_2.idl
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
 - d3d11_2.h
api_name:
 - ID3D11DeviceContext2.SetMarkerInt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext2::SetMarkerInt


## -description


Allows applications to annotate graphics commands.


## -parameters




### -param pLabel [in]

An optional string that will be logged to <a href="ac99a063-e2d2-40cc-b659-d23c2f783f92">ETW</a> when ETW logging is active. If <b>‘#d’</b> appears in the string, it will be replaced by the value of the <i>Data</i> parameter similar to the way <b>printf</b> works.


### -param Data

A signed data value that will be logged to ETW when ETW logging is active.


## -returns



This method does not return a value.




## -remarks



<b>SetMarkerInt</b> allows applications to annotate graphics commands, in order to provide more context to what the GPU is executing. When ETW logging or a support tool is enabled, an additional marker is correlated between the CPU and GPU timelines. The <i>pLabel</i> and <i>Data</i> value are logged to ETW. When the appropriate ETW logging is not enabled, this method does nothing.




## -see-also




<a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a>
 

 

