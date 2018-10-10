---
UID: NF:d2d1effectauthor.ID2D1RenderInfo.SetInstructionCountHint
title: ID2D1RenderInfo::SetInstructionCountHint
author: windows-sdk-content
description: Provides an estimated hint of shader execution cost to D2D.
old-location: direct2d\id2d1renderinfo_setinstructioncounthint.htm
tech.root: Direct2D
ms.assetid: 44077C5C-E3AA-4AE6-B772-BF2669B205B3
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ID2D1RenderInfo interface [Direct2D],SetInstructionCountHint method, ID2D1RenderInfo.SetInstructionCountHint, ID2D1RenderInfo::SetInstructionCountHint, SetInstructionCountHint, SetInstructionCountHint method [Direct2D], SetInstructionCountHint method [Direct2D],ID2D1RenderInfo interface, d2d1effectauthor/ID2D1RenderInfo::SetInstructionCountHint, direct2d.id2d1renderinfo_setinstructioncounthint
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1RenderInfo.SetInstructionCountHint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderInfo::SetInstructionCountHint


## -description


Provides an estimated hint of shader execution cost to D2D.


## -parameters




### -param instructionCount

Type: <b>UINT32</b>

An approximate instruction count of the associated shader.


## -returns



This method does not return a value.




## -remarks



The instruction count may be set according to the number of instructions in the shader.  This information is used as a hint when rendering extremely large images.  Calling this API is optional, but it may  improve performance if you provide an accurate number.



<div class="alert"><b>Note</b>  Instructions that occur in a loop should be counted according to the number of loop iterations.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/26FB6D27-7EE0-43DA-A575-D9FF77846A16">ID2D1RenderInfo</a>
 

 

