---
UID: NF:msinkaut.IInkDisp.Clone
title: IInkDisp::Clone
author: windows-sdk-content
description: Creates a duplicate InkDisp object.
old-location: tablet\inkdisp_clone.htm
old-project: tablet
ms.assetid: f3ec6b42-2b5d-459e-ba09-88c27b125c40
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: Clone, Clone method [Tablet PC], Clone method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],Clone method, IInkDisp.Clone, IInkDisp::Clone, f3ec6b42-2b5d-459e-ba09-88c27b125c40, msinkaut/IInkDisp::Clone, tablet.inkdisp_clone
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
 - IInkDisp.Clone
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkDisp::Clone


## -description



Creates a duplicate <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.




## -parameters




### -param NewInk [out, retval]

When this method returns, contains a pointer to the newly created <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object was not registered.

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
</table>
 




## -remarks



The <b>Clone</b> method is defined for the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a>, <a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes</a>, and <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> objects. The <b>Clone</b> method returns an exact copy of the original object.

In most scenarios, the duplicate object is an exact copy of the original object, but no relation between the two objects exists. See the remarks section of this topic for details on exceptions to this.


<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object: The only scenario in which the duplicate <b>InkDisp</b> object is not an exact copy of the original object is when a dirty <b>InkDisp</b> object is cloned. In this case, the duplicate <b>InkDisp</b> object's <a href="https://msdn.microsoft.com/3399219f-96a5-4c66-8e41-89927ea1020d">Dirty</a> property is <b>FALSE</b>. All other properties of the cloned <b>InkDisp</b> object are exact copies.




## -see-also




<a href="https://msdn.microsoft.com/3399219f-96a5-4c66-8e41-89927ea1020d">Dirty Property</a>



<a href="tablet.iinkdisp">IInkDisp</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/b249edd9-dfa4-4538-9764-a4365f9df527">ModifyDrawingAttributes Method</a>
 

 

