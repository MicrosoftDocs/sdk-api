---
UID: NF:strmif.IDvdInfo2.GetButtonAtPosition
title: IDvdInfo2::GetButtonAtPosition
author: windows-driver-content
description: The GetButtonAtPosition method retrieves the button located at the specified point within the display window.
old-location: dshow\idvdinfo2_getbuttonatposition.htm
old-project: DirectShow
ms.assetid: f9c506b3-c9d9-4dc2-b318-f987ab8636dc
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetButtonAtPosition, GetButtonAtPosition method [DirectShow], GetButtonAtPosition method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetButtonAtPosition method, IDvdInfo2.GetButtonAtPosition, IDvdInfo2::GetButtonAtPosition, IDvdInfo2GetButtonAtPosition, dshow.idvdinfo2_getbuttonatposition, strmif/IDvdInfo2::GetButtonAtPosition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDvdInfo2.GetButtonAtPosition
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetButtonAtPosition


## -description



The <code>GetButtonAtPosition</code> method retrieves the button located at the specified point within the display window.




## -parameters




### -param point [in]

Current mouse pointer position as retrieved through the Win32 WM_MOUSEMOVE message.


### -param pulButtonIndex






#### - puButtonIndex [out]

Receives the index (from 1 through 36) of the button at the current mouse pointer position.


## -returns



Returns one of the following <b>HRESULT</b> values.

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>puButtonIndex</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NO_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
No button at <i>point</i>.

</td>
</tr>
</table>
 




## -remarks



This method is typically called in response to a mouse pointer move within a DVD menu display window. Be sure to check for success in the <b>HRESULT</b> before trying to retrieve the button number; this method only sets the value of <i>puButtonIndex</i> if a button is found at the specified point. DVD buttons do not necessarily have highlighted rectangles, button rectangles can overlap, and button rectangles do not always correspond to the visual representation of the buttons.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

