---
UID: NF:msinkaut.IInkDisp.ExtractWithRectangle
title: IInkDisp::ExtractWithRectangle
author: windows-sdk-content
description: Cuts or copies strokes from an existing InkDisp object and pastes them into a new InkDisp object, by using the known rectangle to determine which strokes to extract.
old-location: tablet\inkdisp_extractwithrectangle.htm
tech.root: tablet
ms.assetid: b32467a8-a677-4a80-8029-d364e6e372c6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ExtractWithRectangle, ExtractWithRectangle method [Tablet PC], ExtractWithRectangle method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],ExtractWithRectangle method, IInkDisp.ExtractWithRectangle, IInkDisp::ExtractWithRectangle, b32467a8-a677-4a80-8029-d364e6e372c6, msinkaut/IInkDisp::ExtractWithRectangle, tablet.inkdisp_extractwithrectangle
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkDisp.ExtractWithRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDisp::ExtractWithRectangle


## -description



Cuts or copies strokes from an existing <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object and pastes them into a new <b>InkDisp</b> object, by using the known rectangle to determine which strokes to extract.




## -parameters




### -param Rectangle [in]

Specifies the <a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle</a> object which delimits the ink to extract from the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.


### -param extractFlags [in, optional]

Optional. Specifies the <a href="https://msdn.microsoft.com/22dd44bb-2175-420f-b5fd-4648ebe489a5">InkExtractFlags</a> enumeration type, which determines whether the ink should be cut or copied from the existing <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object. The default value is IEF_DEFAULT, which cuts the strokes from the existing <b>InkDisp</b> object.


### -param ExtractedInk [out, retval]

When this method returns, contains a pointer to an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object that contains the extracted collection of strokes.


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
<dt><b>E_INK_SOME_STROKES_NOT_EXTRACTED</b></dt>
</dl>
</td>
<td width="60%">
Not all strokes were extracted.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid extraction flags.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The Ink object was not registered.

</td>
</tr>
</table>
 




## -remarks



The new <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object retains the drawing attributes, properties, and coordinates of the original <b>InkDisp</b> object.

This method is useful for creating a new <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object without the deleted or cut strokes from the original object.

To extract strokes from a known collection of strokes, call the <a href="https://msdn.microsoft.com/1cb109e5-5193-4022-a3b1-ade9be1337e8">ExtractStrokes Method</a>.

Only the portion of a stroke that is within the rectangle is added to the new <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.

When the <i>extractFlags</i> parameter is <a href="https://msdn.microsoft.com/22dd44bb-2175-420f-b5fd-4648ebe489a5">RemoveFromOriginal</a> or <b>Default</b>, any strokes that cross the rectangle are split and the portion within the rectangle removed from the existing <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.




## -see-also




<a href="https://msdn.microsoft.com/1cb109e5-5193-4022-a3b1-ade9be1337e8">ExtractStrokes Method</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846797(v=VS.85).aspx">IInkDisp</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/22dd44bb-2175-420f-b5fd-4648ebe489a5">InkExtractFlags Enumeration</a>



<a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

