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

# ITfMenu::AddMenuItem


## -description




## -parameters




### -param uId [in]

Contains the menu item identifier.


### -param dwFlags [in]

Contains zero or a combination of one or more of the <a href="https://msdn.microsoft.com/f8f3f397-b84e-4635-b454-31369c679ce2">TF_LBMENUF_*</a> values that specify the type and state of the menu item.


### -param hbmp [in]

Contains the handle of the bitmap drawn for the menu item. If this is <b>NULL</b>, no bitmap is displayed for the menu item.


### -param hbmpMask [in]

Contains the handle of the mask bitmap. This is a monochrome bitmap that functions as a mask for <i>hbmp</i>. Each black pixel in this bitmap will cause the corresponding pixel in <i>hbmp</i> to be displayed in its normal color. Each white pixel in this bitmap will cause the corresponding pixel in <i>hbmp</i> to be displayed in the inverse of its normal color.

To have the bitmap displayed without any color conversion, create a monochrome bitmap the same size as <i>hbmp</i> and set each pixel to black (RGB(0, 0, 0)).

If <i>hbmp</i> is <b>NULL</b>, this parameter is ignored.


### -param pch [in]

Pointer to a <b>WCHAR</b> buffer that contains the text to be displayed for the menu item. The length of the text is specified by <i>cch</i>.


### -param cch [in]

Specifies the length, in <b>WCHAR</b>, of the menu item text in <i>pch</i>.


### -param ppMenu

[in, out] Pointer to an <a href="https://msdn.microsoft.com/303115e1-8d52-4a0a-b05e-b5c92b8b3e2a">ITfMenu</a> interface pointer that receives the submenu object. This parameter is not used and must be <b>NULL</b> if <i>dwFlags</i> does not contain <b>TF_LBMENUF_SUBMENU</b>.

If the submenu item is successfully created, this parameter receives an <a href="https://msdn.microsoft.com/303115e1-8d52-4a0a-b05e-b5c92b8b3e2a">ITfMenu</a> object that the caller uses to add items to the submenu.

If <i>dwFlags</i> contains <b>TF_LBMENUF_SUBMENU</b>, this value must be initialized to <b>NULL</b> prior to calling this method because, in most cases, this is a marshalled call. Not initializing this variable results in the marshaller attempting to access random memory.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/303115e1-8d52-4a0a-b05e-b5c92b8b3e2a">ITfMenu</a>



<a href="https://msdn.microsoft.com/f8f3f397-b84e-4635-b454-31369c679ce2">
        TF_LBMENUF_* Constants
      </a>
 

 

