---
UID: NE:d3d10sdklayers.D3D10_MESSAGE_SEVERITY
title: D3D10_MESSAGE_SEVERITY
author: windows-sdk-content
description: Debug message severity levels for an information queue.
old-location: direct3d10\d3d10_message_severity.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_message_severity.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D3D10_MESSAGE_SEVERITY, D3D10_MESSAGE_SEVERITY enumeration [Direct3D 10], D3D10_MESSAGE_SEVERITY_CORRUPTION, D3D10_MESSAGE_SEVERITY_ERROR, D3D10_MESSAGE_SEVERITY_INFO, D3D10_MESSAGE_SEVERITY_WARNING, b48ff3e8-3124-4d3c-9284-db459579b3d2, d3d10sdklayers/D3D10_MESSAGE_SEVERITY, d3d10sdklayers/D3D10_MESSAGE_SEVERITY_CORRUPTION, d3d10sdklayers/D3D10_MESSAGE_SEVERITY_ERROR, d3d10sdklayers/D3D10_MESSAGE_SEVERITY_INFO, d3d10sdklayers/D3D10_MESSAGE_SEVERITY_WARNING, direct3d10.d3d10_message_severity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d10sdklayers.h
req.include-header: D3D10.h
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
req.typenames: D3D10_MESSAGE_SEVERITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10sdklayers.h
api_name:
 - D3D10_MESSAGE_SEVERITY
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10_MESSAGE_SEVERITY enumeration


## -description


Debug message severity levels for an information queue.


## -enum-fields




### -field D3D10_MESSAGE_SEVERITY_CORRUPTION

Defines some type of corruption which has occurred.


### -field D3D10_MESSAGE_SEVERITY_ERROR

Defines an error message.


### -field D3D10_MESSAGE_SEVERITY_WARNING

Defines a warning message.


### -field D3D10_MESSAGE_SEVERITY_INFO

Defines an information message.


### -field D3D10_MESSAGE_SEVERITY_MESSAGE




## -remarks



Use these values to allow or deny message categories to pass through the storage and retrieval filters for an information queue (see <a href="https://msdn.microsoft.com/en-us/library/Bb205313(v=VS.85).aspx">D3D10_INFO_QUEUE_FILTER</a>). This API is used by <a href="https://msdn.microsoft.com/en-us/library/Bb173780(v=VS.85).aspx">ID3D10InfoQueue::AddApplicationMessage</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205150(v=VS.85).aspx">Core Enumerations</a>
 

 

