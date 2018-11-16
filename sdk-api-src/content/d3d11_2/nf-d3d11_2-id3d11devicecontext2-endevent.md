---
UID: NF:d3d11_2.ID3D11DeviceContext2.EndEvent
title: ID3D11DeviceContext2::EndEvent
author: windows-sdk-content
description: Allows applications to annotate the end of a range of graphics commands.
old-location: direct3d11\id3d11devicecontext2_endevent.htm
tech.root: direct3d11
ms.assetid: 1684ee4b-637d-4764-bb69-6ebc5c2985f1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EndEvent, EndEvent method [Direct3D 11], EndEvent method [Direct3D 11],ID3D11DeviceContext2 interface, ID3D11DeviceContext2 interface [Direct3D 11],EndEvent method, ID3D11DeviceContext2.EndEvent, ID3D11DeviceContext2::EndEvent, d3d11_2/ID3D11DeviceContext2::EndEvent, direct3d11.id3d11devicecontext2_endevent
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
 - ID3D11DeviceContext2.EndEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11_2.h
: 
- ID3D11DeviceContext2.EndEvent
: 
---

# ID3D11DeviceContext2::EndEvent


## -description


Allows applications to annotate the end of a range of graphics commands.


## -parameters






## -returns



This method does not return a value.




## -remarks



<b>EndEvent</b> allows applications to annotate the end of a range of graphics commands, in order to provide more context to what the GPU is executing. When the appropriate <a href="ac99a063-e2d2-40cc-b659-d23c2f783f92">ETW</a> logging is not enabled, this method does nothing. When ETW logging is enabled, an additional marker is correlated between the CPU and GPU timelines.




## -see-also




<a href="https://msdn.microsoft.com/8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA">ID3D11DeviceContext2</a>
 

 

