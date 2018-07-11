---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.SetBreakOnSeverity
title: ID3D10InfoQueue::SetBreakOnSeverity
author: windows-sdk-content
description: Set a message severity level to break on when a message with that severity level passes through the storage filter.
old-location: direct3d10\id3d10infoqueue_setbreakonseverity.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_setbreakonseverity.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ID3D10InfoQueue interface [Direct3D 10],SetBreakOnSeverity method, ID3D10InfoQueue.SetBreakOnSeverity, ID3D10InfoQueue::SetBreakOnSeverity, SetBreakOnSeverity, SetBreakOnSeverity method [Direct3D 10], SetBreakOnSeverity method [Direct3D 10],ID3D10InfoQueue interface, a333f38c-3dea-80fe-c7bb-b11dfec7e140, d3d10sdklayers/ID3D10InfoQueue::SetBreakOnSeverity, direct3d10.id3d10infoqueue_setbreakonseverity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10sdklayers.h
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
req.typenames: D3D10_MESSAGE_SEVERITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10InfoQueue.SetBreakOnSeverity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10InfoQueue::SetBreakOnSeverity


## -description


Set a message severity level to break on when a message with that severity level passes through the storage filter.


## -parameters




### -param Severity [in]

Type: <b><a href="https://msdn.microsoft.com/548487cb-1315-45b2-86df-f32d129a1212">D3D10_MESSAGE_SEVERITY</a></b>

Message severity level to break on (see <a href="https://msdn.microsoft.com/548487cb-1315-45b2-86df-f32d129a1212">D3D10_MESSAGE_SEVERITY</a>).


### -param bEnable [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Turns this breaking condition on or off (true for on, false for off).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>
 

 

