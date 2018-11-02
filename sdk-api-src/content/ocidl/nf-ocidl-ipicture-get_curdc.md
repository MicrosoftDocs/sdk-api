---
UID: NF:ocidl.IPicture.get_CurDC
title: IPicture::get_CurDC
author: windows-sdk-content
description: Retrieves the handle of the current device context. This property is valid only for bitmap pictures.
old-location: com\ipicture_get_curdc.htm
tech.root: com
ms.assetid: a5c13a54-692d-423f-824d-5a96c137dec9
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IPicture interface [COM],get_CurDC method, IPicture.get_CurDC, IPicture::get_CurDC, _ctrl_ipicture_get_curdc, com.ipicture_get_curdc, get_CurDC, get_CurDC method [COM], get_CurDC method [COM],IPicture interface, ocidl/IPicture::get_CurDC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPicture.get_CurDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPicture::get_CurDC


## -description


Retrieves the handle of the current device context. This property is valid only for bitmap pictures.


## -parameters




### -param phDC [out]

A pointer a variable that receives the device context.


## -returns



This method supports the standard return value E_FAIL, as well as the following values.

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
The attribute bits were returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>phDC</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The CurDC property and the <a href="https://msdn.microsoft.com/4168dbf7-ccc3-49ee-9b04-b0370eb389af">IPicture::SelectPicture</a> method exist to circumvent restrictions in Windows; specifically, that an object can only be selected into exactly one device context at a time. In some cases, a picture object may be permanently selected into a particular device context (for example, a control may use a certain picture for a background). To use this picture property elsewhere, it must be temporarily deselected from its old device context, selected into the new device context for the operation, then reselected back into the old device context. The <b>IPicture::get_CurDC</b> method returns the device context handle into which the picture is currently selected. The <b>IPicture::SelectPicture</b> method selects the picture into a new device context, returning the old device context and the picture's GDI handle. The caller should select the picture back into the old device context when the caller is done with it, as is normal for Windows code.

<h3><a id="Notes_to_Callers_"></a><a id="notes_to_callers_"></a><a id="NOTES_TO_CALLERS_"></a>Notes to Callers
</h3>
The caller always owns any device contexts passed between it and the picture object. Because the picture object maintains a copy of the HDC, the caller should use a memory device context (created with the <a href="https://msdn.microsoft.com/6ddc3705-2995-41af-af94-258aed597e17">CreateCompatibleDC</a> function) and not a screen device context (from <a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a>, <a href="https://msdn.microsoft.com/6fc443c8-da97-4196-a9ed-179a4e583849">CreateDC</a>, or <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>), because the screen device contexts are a limited system resource.




## -see-also




<a href="https://msdn.microsoft.com/42e3cd0e-2413-494a-8be8-2952089e02d2">IPicture</a>



<a href="https://msdn.microsoft.com/4168dbf7-ccc3-49ee-9b04-b0370eb389af">IPicture::SelectPicture</a>
 

 

