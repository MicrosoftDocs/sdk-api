---
UID: NF:msinkaut.IInkTransform.SetTransform
title: IInkTransform::SetTransform
author: windows-sdk-content
description: Modifies the InkTransform member data.
old-location: tablet\inktransform_settransform.htm
old-project: tablet
ms.assetid: 5b734703-4117-4668-b881-4ba4e1c65189
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: 5b734703-4117-4668-b881-4ba4e1c65189, IInkTransform interface [Tablet PC],SetTransform method, IInkTransform.SetTransform, IInkTransform::SetTransform, SetTransform, SetTransform method [Tablet PC], SetTransform method [Tablet PC],IInkTransform interface, msinkaut/IInkTransform::SetTransform, tablet.inktransform_settransform
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
 - IInkTransform.SetTransform
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkTransform::SetTransform


## -description



Modifies the <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> member data.



An <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object represents a 3×3 matrix that, in turn, represents an affine transformation. The object stores only six of the nine numbers in a 3×3 matrix because all 3×3 matrices that represent affine transformations have the same third column (0, 0, 1).


## -parameters




### -param eM11 [in]

The element in the first row, first column.


### -param eM12 [in]

The element in the first row, second column.


### -param eM21 [in]

The element in the second row, first column.


### -param eM22 [in]

The element in the second row, second column.


### -param eDx [in]

The element in the third row, first column.


### -param eDy [in]

The element in the third row, second column.


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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d6aec579-7fa4-4cfb-8f63-2810b0c40103">GetTransform Method</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846808(v=VS.85).aspx">IInkTransform</a>



<a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform Class</a>
 

 

