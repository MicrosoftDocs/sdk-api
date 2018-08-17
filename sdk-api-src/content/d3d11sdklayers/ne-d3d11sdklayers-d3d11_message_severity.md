---
UID: NE:d3d11sdklayers.D3D11_MESSAGE_SEVERITY
title: D3D11_MESSAGE_SEVERITY
author: windows-sdk-content
description: Debug message severity levels for an information queue.
old-location: direct3d11\d3d11_message_severity.htm
old-project: direct3d11
ms.assetid: 63143187-8e16-4ba4-aec5-8530ed31accb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 5817bf39-bfcb-e96c-175e-08c952303b59, D3D11_MESSAGE_SEVERITY, D3D11_MESSAGE_SEVERITY enumeration [Direct3D 11], D3D11_MESSAGE_SEVERITY_CORRUPTION, D3D11_MESSAGE_SEVERITY_ERROR, D3D11_MESSAGE_SEVERITY_INFO, D3D11_MESSAGE_SEVERITY_MESSAGE, D3D11_MESSAGE_SEVERITY_WARNING, d3d11sdklayers/D3D11_MESSAGE_SEVERITY, d3d11sdklayers/D3D11_MESSAGE_SEVERITY_CORRUPTION, d3d11sdklayers/D3D11_MESSAGE_SEVERITY_ERROR, d3d11sdklayers/D3D11_MESSAGE_SEVERITY_INFO, d3d11sdklayers/D3D11_MESSAGE_SEVERITY_MESSAGE, d3d11sdklayers/D3D11_MESSAGE_SEVERITY_WARNING, direct3d11.d3d11_message_severity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d11sdklayers.h
req.include-header: 
req.redist: 
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
req.typenames: D3D11_MESSAGE_SEVERITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11SDKLayers.h
api_name:
 - D3D11_MESSAGE_SEVERITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_MESSAGE_SEVERITY enumeration


## -description


Debug message severity levels for an information queue.


## -enum-fields




### -field D3D11_MESSAGE_SEVERITY_CORRUPTION

Defines some type of corruption which has occurred.


### -field D3D11_MESSAGE_SEVERITY_ERROR

Defines an error message.


### -field D3D11_MESSAGE_SEVERITY_WARNING

Defines a warning message.


### -field D3D11_MESSAGE_SEVERITY_INFO

Defines an information message.


### -field D3D11_MESSAGE_SEVERITY_MESSAGE

Defines a message other than corruption, error, warning, or information.

<b>Direct3D 11:  </b>This value is not supported until Direct3D 11.1.


## -remarks



Use these values to allow or deny message categories to pass through the storage and retrieval filters for an information queue (see <a href="https://msdn.microsoft.com/en-us/library/Ff476177(v=VS.85).aspx">D3D11_INFO_QUEUE_FILTER</a>). This API is used by <a href="https://msdn.microsoft.com/en-us/library/Ff476539(v=VS.85).aspx">ID3D11InfoQueue::AddApplicationMessage</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476157(v=VS.85).aspx">Layer Enumerations</a>
 

 

