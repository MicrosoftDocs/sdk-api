---
UID: NF:d2d1_1.ID2D1DeviceContext.GetEffectRequiredInputRectangles
title: ID2D1DeviceContext::GetEffectRequiredInputRectangles
author: windows-sdk-content
description: Returns the input rectangles that are required to be supplied by the caller to produce the given output rectangle.
old-location: direct2d\id2d1devicecontext_geteffectrequiredinputrectangles.htm
tech.root: direct2d
ms.assetid: B34548A9-1E23-496F-A1D9-87B74EF67C72
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetEffectRequiredInputRectangles, GetEffectRequiredInputRectangles method [Direct2D], GetEffectRequiredInputRectangles method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],GetEffectRequiredInputRectangles method, ID2D1DeviceContext.GetEffectRequiredInputRectangles, ID2D1DeviceContext::GetEffectRequiredInputRectangles, d2d1_1/ID2D1DeviceContext::GetEffectRequiredInputRectangles, direct2d.id2d1devicecontext_geteffectrequiredinputrectangles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext.GetEffectRequiredInputRectangles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext::GetEffectRequiredInputRectangles


## -description


Returns the input rectangles that are required to be supplied by the caller to produce the given output rectangle. 
        


## -parameters




### -param renderEffect [in]

Type: <b><a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>*</b>

The image whose output is being rendered.


### -param renderImageRectangle [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The portion of the output image whose inputs are being inspected.


### -param inputDescriptions [in]

Type: <b>const <a href="https://msdn.microsoft.com/2ce9405a-e36d-4b9e-b9d2-2a58b78696ac">D2D1_EFFECT_INPUT_DESCRIPTION</a>*</b>

A list of the inputs whos rectangles are being queried.
          


### -param requiredInputRects [out]

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

The input rectangles returned to the caller.


### -param inputCount

Type: <b>UINT32</b>

The number of inputs.


## -returns



Type: <b>HRESULT</b>

A failure code, this will typically only be because an effect in the chain returned some error.
            




## -remarks



The caller should be very careful not to place a reliance on the required input rectangles returned. 
      Small changes for correctness to an effect's behavior can result in different rectangles being returned. 
      In addition, different kinds of optimization applied inside the render can also influence the result. 




## -see-also




<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

