---
UID: NF:msinkaut.IInkTransform.Translate
title: IInkTransform::Translate
author: windows-sdk-content
description: Applies a translation to a transform.
old-location: tablet\inktransform_translate.htm
old-project: tablet
ms.assetid: 3125e27b-a280-43bc-99d7-a6b5697366b2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 3125e27b-a280-43bc-99d7-a6b5697366b2, IInkTransform interface [Tablet PC],Translate method, IInkTransform.Translate, IInkTransform::Translate, Translate, Translate method [Tablet PC], Translate method [Tablet PC],IInkTransform interface, msinkaut/IInkTransform::Translate, tablet.inktransform_translate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.redist: 
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
 - IInkTransform.Translate
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkTransform::Translate


## -description



Applies a translation to a transform.




## -parameters




### -param HorizontalComponent [in]

The horizontal component of the translation.


### -param VerticalComponent [in]

The vertical component of the translation.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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




<a href="https://msdn.microsoft.com/en-us/library/Mt846808(v=VS.85).aspx">IInkTransform</a>



<a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform Class</a>
 

 

