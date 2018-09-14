---
UID: NF:d2d1_1helper.RenderingControls
title: RenderingControls function
author: windows-sdk-content
description: Returns a filled D2D1_RENDERING_CONTROLS structure.
old-location: direct2d\renderingcontrols.htm
tech.root: Direct2D
ms.assetid: 5004EA84-216C-4758-8AA1-7E823583871E
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: RenderingControls, RenderingControls function [Direct2D], d2d1_1helper/RenderingControls, direct2d.renderingcontrols
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1_1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - RenderingControls
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RenderingControls function


## -description


Returns a filled D2D1_RENDERING_CONTROLS structure.


## -parameters




### -param bufferPrecision

Type: <b><a href="https://msdn.microsoft.com/a2a4b4fd-685d-4068-b1f5-609e6ab024e2">D2D1_BUFFER_PRECISION</a></b>

The buffer precision used by default if the buffer precision is not otherwise specified by the effect or the transform.


### -param tileSize

Type: <b><a href="https://msdn.microsoft.com/e28da5ee-7d68-4ec5-b477-c6ead0c725e6">D2D1_SIZE_U</a></b>

The minimum tile allocation size to be used by the imaging effect renderer.


## -returns



Type: <b><a href="https://msdn.microsoft.com/e563cbb0-2ee0-43d8-978c-0bde1950a926">D2D1_RENDERING_CONTROLS</a></b>

Describes limitations to be applied to an imaging effect renderer.



