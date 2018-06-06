---
UID: NF:strmif.IDvdInfo2.GetButtonRect
title: IDvdInfo2::GetButtonRect
author: windows-sdk-content
description: The GetButtonRect method retrieves the rectangle coordinates for the specified menu button. Note  This method is currently not implemented. .
old-location: dshow\idvdinfo2_getbuttonrect.htm
old-project: DirectShow
ms.assetid: 8825979c-2a98-462a-acf9-939c81ece89a
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetButtonRect, GetButtonRect method [DirectShow], GetButtonRect method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetButtonRect method, IDvdInfo2.GetButtonRect, IDvdInfo2::GetButtonRect, IDvdInfo2GetButtonRect, dshow.idvdinfo2_getbuttonrect, strmif/IDvdInfo2::GetButtonRect
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdInfo2.GetButtonRect
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetButtonRect


## -description



The <code>GetButtonRect</code> method retrieves the rectangle coordinates for the specified menu button. 


<div class="alert"><b>Note</b>  This method is currently not implemented.</div>
<div> </div>





## -parameters




### -param ulButton [in]

Specifies the menu button.


### -param pRect [out]

Pointer to a variable of type RECT that receives the coordinates of the button's rectangle.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is currently not implemented

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

