---
UID: NF:msinkaut.IInkPicture.GetWindowInputRectangle
title: IInkPicture::GetWindowInputRectangle
author: windows-sdk-content
description: Retrieves the window rectangle, in pixels, within which ink is drawn.
old-location: tablet\inkpicture_getwindowinputrectangle.htm
tech.root: tablet
ms.assetid: 975e5921-cc76-4b38-9f3c-364e8704ba03
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 0f47b4c7-7ba1-44a6-8f62-9e97c318bd2c, GetWindowInputRectangle, GetWindowInputRectangle method [Tablet PC], GetWindowInputRectangle method [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],GetWindowInputRectangle method, IInkPicture.GetWindowInputRectangle, IInkPicture::GetWindowInputRectangle, msinkaut/IInkPicture::GetWindowInputRectangle, tablet.inkpicture_getwindowinputrectangle
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
 - IInkPicture.GetWindowInputRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- msinkaut.h
: 
- IInkPicture.GetWindowInputRectangle
: 
---

# IInkPicture::GetWindowInputRectangle


## -description



Retrieves the window rectangle, in pixels, within which ink is drawn.




## -parameters




### -param WindowInputRectangle [out]

Gets the rectangle, of type <a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle</a>, on which ink is drawn.


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
A parameter contains an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The InkRectangle object is not registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurs inside the method.

</td>
</tr>
</table>
 




## -remarks



You must first allocate the rectangle before passing it on to this method.

By default, the window input rectangle is set to {0,0,0,0}. This default rectangle maps to the size of the entire window.

If you call <b>GetWindowInputRectangle</b> before you call the <a href="https://msdn.microsoft.com/3602a550-d37b-4a78-b949-04f5e3cb923a">SetWindowInputRectangle</a> method, this method gets a rectangle with the default coordinates.




## -see-also




<a href="https://msdn.microsoft.com/EA6AC3DD-5F13-442A-B93D-FF0A5333609A">IInkPicture</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>



<a href="https://msdn.microsoft.com/3602a550-d37b-4a78-b949-04f5e3cb923a">SetWindowInputRectangle Method</a>
 

 

