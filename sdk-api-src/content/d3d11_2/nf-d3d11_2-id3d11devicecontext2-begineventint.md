---
UID: NF:d3d11_2.ID3D11DeviceContext2.BeginEventInt
title: ID3D11DeviceContext2::BeginEventInt (d3d11_2.h)
author: windows-sdk-content
description: Allows applications to annotate the beginning of a range of graphics commands.
old-location: direct3d11\id3d11devicecontext2_begineventint.htm
tech.root: direct3d11
ms.assetid: 9a45e16f-a598-4196-ad9c-8a157ae94de0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BeginEventInt, BeginEventInt method [Direct3D 11], BeginEventInt method [Direct3D 11],ID3D11DeviceContext2 interface, ID3D11DeviceContext2 interface [Direct3D 11],BeginEventInt method, ID3D11DeviceContext2.BeginEventInt, ID3D11DeviceContext2::BeginEventInt, d3d11_2/ID3D11DeviceContext2::BeginEventInt, direct3d11.id3d11devicecontext2_begineventint
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
 - ID3D11DeviceContext2.BeginEventInt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11DeviceContext2::BeginEventInt


## -description


Allows applications to annotate the beginning of a range of graphics commands.


## -parameters




### -param pLabel [in]

An optional string that will be logged to <a href="https://msdn.microsoft.com/library/ms751538(v=VS.85).aspx">ETW</a> when ETW logging is active. If <b>‘#d’</b> appears in the string, it will be replaced by the value of the <i>Data</i> parameter similar to the way <b>printf</b> works.


### -param Data

A signed data value that will be logged to ETW when ETW logging is active.


## -returns



This method does not return a value.




## -remarks



<b>BeginEventInt</b> allows applications to annotate the beginning of a range of graphics commands, in order to provide more context to what the GPU is executing. When <a href="https://msdn.microsoft.com/library/ms751538(v=VS.85).aspx">ETW</a> logging (or a supported tool) is enabled, an additional marker is correlated between the CPU and GPU timelines. The <i>pLabel</i> and <i>Data</i> value are logged to ETW. When the appropriate ETW logging is not enabled, this method does nothing.




## -see-also




<a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a>
 

 

