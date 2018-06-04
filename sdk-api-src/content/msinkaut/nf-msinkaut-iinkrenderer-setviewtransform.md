---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IInkRenderer::SetViewTransform


## -description



Sets the <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object that represents the view transform that is used to render ink.




## -parameters




### -param ViewTransform






#### - viewTransform [in]

The <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object that represents the geometric transformation - rotation, scaling, shear, and reflection - values to use to transform the stroke coordinates within the ink space.

A <b>NULL</b> value for the <i>viewTransform</i> parameter correlates to the identity transform.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>viewTransform</i> does not point to a compatible <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object.

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
 




## -remarks



The transformation applies to both the points and pen width.

View transformation occurs after object transformation.

The pen width is calculated by multiplying the specified pen width (or default of 53, if unspecified) by the square root of the determinant of the view transform.

It is problematic to call this method in response to SENT message.  Test whether you are processing a SENT message
			  by calling <a href="https://msdn.microsoft.com/6625958c-9ebb-4fb1-806f-625fe9e69c22">InSendMesssageEx</a> and then POST the message to yourself if the message was SENT.




## -see-also




<a href="https://msdn.microsoft.com/11195fa1-ca59-4da6-8454-6209c75ccc67">GetObjectTransform Method</a>



<a href="https://msdn.microsoft.com/8a4d768d-09b6-45e1-b412-e267d92cc3ef">GetViewTransform Method</a>



<a href="tablet.iinkrenderer">IInkRenderer</a>



<a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer Class</a>
 

 

