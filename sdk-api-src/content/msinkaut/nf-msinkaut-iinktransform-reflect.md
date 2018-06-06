---
UID: NF:msinkaut.IInkTransform.Reflect
title: IInkTransform::Reflect
author: windows-sdk-content
description: Performs reflection on a transform in either horizontal or vertical directions.
old-location: tablet\inktransform_reflect.htm
old-project: tablet
ms.assetid: ebecd285-4dc4-4f4a-9d07-a3287b0438e9
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: IInkTransform interface [Tablet PC],Reflect method, IInkTransform.Reflect, IInkTransform::Reflect, Reflect, Reflect method [Tablet PC], Reflect method [Tablet PC],IInkTransform interface, ebecd285-4dc4-4f4a-9d07-a3287b0438e9, msinkaut/IInkTransform::Reflect, tablet.inktransform_reflect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkTransform.Reflect
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkTransform::Reflect


## -description



Performs reflection on a transform in either horizontal or vertical directions.




## -parameters




### -param Horizontally [in]

<b>VARIANT_TRUE</b> to reflect in the horizontal direction; otherwise, <b>VARIANT_FALSE</b>.


### -param Vertically [in]

<b>VARIANT_TRUE</b> to reflect in the vertical direction; otherwise, <b>VARIANT_FALSE</b>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid VARIANT_BOOL variants.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>
 




## -see-also




<a href="tablet.iinktransform">IInkTransform</a>



<a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform Class</a>
 

 

