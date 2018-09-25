---
UID: NF:d2d1effectauthor.ID2D1ConcreteTransform.SetOutputBuffer
title: ID2D1ConcreteTransform::SetOutputBuffer
author: windows-sdk-content
description: Sets the properties of the output buffer of the specified transform node.
old-location: direct2d\id2d1concretetransform_setoutputbuffer.htm
tech.root: direct2d
ms.assetid: DCA691ED-B9DF-4B1A-8662-0981BFB359CE
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ID2D1ConcreteTransform interface [Direct2D],SetOutputBuffer method, ID2D1ConcreteTransform.SetOutputBuffer, ID2D1ConcreteTransform::SetOutputBuffer, SetOutputBuffer, SetOutputBuffer method [Direct2D], SetOutputBuffer method [Direct2D],ID2D1ConcreteTransform interface, d2d1effectauthor/ID2D1ConcreteTransform::SetOutputBuffer, direct2d.id2d1concretetransform_setoutputbuffer
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
 - ID2D1ConcreteTransform.SetOutputBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1ConcreteTransform::SetOutputBuffer


## -description


Sets the properties of the output buffer of the specified transform node.


## -parameters




### -param bufferPrecision

Type: <b><a href="https://msdn.microsoft.com/a2a4b4fd-685d-4068-b1f5-609e6ab024e2">D2D1_BUFFER_PRECISION</a></b>

The number of bits and the type of the output buffer.


### -param channelDepth

Type: <b><a href="https://msdn.microsoft.com/78129b15-a770-49c0-b58b-8cb850f80006">D2D1_CHANNEL_DEPTH</a></b>

The number of channels in the output buffer (1 or 4).


## -returns



Type: <b>HRESULT</b>

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>One or more arguments are not valid</td>
</tr>
</table>
 




## -remarks



You can use the <a href="https://msdn.microsoft.com/731A7CF3-03E7-4D38-A8DD-8D207AE90B16">ID2D1EffectContext::IsBufferPrecisionSupported</a> method to see if buffer precision is supported.

The available channel depth and precision depend on the capabilities of the underlying Microsoft Direct3D device.




## -see-also




<a href="https://msdn.microsoft.com/a2a4b4fd-685d-4068-b1f5-609e6ab024e2">D2D1_BUFFER_PRECISION</a>



<a href="https://msdn.microsoft.com/78129b15-a770-49c0-b58b-8cb850f80006">D2D1_CHANNEL_DEPTH</a>



<a href="https://msdn.microsoft.com/5349EF29-767F-4C78-A6F9-B0C6F143E762">ID2D1ConcreteTransform</a>
 

 

