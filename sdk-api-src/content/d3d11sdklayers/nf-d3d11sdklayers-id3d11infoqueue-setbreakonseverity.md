---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.SetBreakOnSeverity
title: ID3D11InfoQueue::SetBreakOnSeverity
author: windows-sdk-content
description: Set a message severity level to break on when a message with that severity level passes through the storage filter.
old-location: direct3d11\id3d11infoqueue_setbreakonseverity.htm
old-project: direct3d11
ms.assetid: de977ab5-a277-41fe-a99d-153fa75fc15a
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 1dc10d17-30bc-4151-6e43-5c1c7fbd518c, ID3D11InfoQueue interface [Direct3D 11],SetBreakOnSeverity method, ID3D11InfoQueue.SetBreakOnSeverity, ID3D11InfoQueue::SetBreakOnSeverity, SetBreakOnSeverity, SetBreakOnSeverity method [Direct3D 11], SetBreakOnSeverity method [Direct3D 11],ID3D11InfoQueue interface, d3d11sdklayers/ID3D11InfoQueue::SetBreakOnSeverity, direct3d11.id3d11infoqueue_setbreakonseverity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11sdklayers.h
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
req.typenames: D3D11_SHADER_TRACKING_RESOURCE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11InfoQueue.SetBreakOnSeverity
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11InfoQueue::SetBreakOnSeverity


## -description


Set a message severity level to break on when a message with that severity level passes through the storage filter.


## -parameters




### -param Severity [in]

Type: <b><a href="https://msdn.microsoft.com/63143187-8e16-4ba4-aec5-8530ed31accb">D3D11_MESSAGE_SEVERITY</a></b>

A <a href="https://msdn.microsoft.com/63143187-8e16-4ba4-aec5-8530ed31accb">D3D11_MESSAGE_SEVERITY</a>, which represents a message severity level to break on.


### -param bEnable [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Turns this breaking condition on or off (true for on, false for off).


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>
 

 

