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

# ITfLangBarItemBalloon::GetPreferredSize


## -description




## -parameters




### -param pszDefault [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure that contains the default size, in pixels, of the balloon.


### -param psz [out]

Pointer to a <b>SIZE</b> structure that recevies the preferred balloon size, in pixels. The <b>cy</b> member of this structure is ignored.


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
</table>
 




## -remarks



This method is required. The balloon must supply the preferred size in response to this method.

To obtain the font used to draw the balloon, call <a href="https://msdn.microsoft.com/b14ddc05-7e7b-4fc6-b7e3-efe892df7e21">GetStockObject</a> with DEFAULT_GUI_FONT. This font can be used to calculate the preferred balloon size at runtime.

If the ballon text will not fit into the preferred size obtained from this method, the language bar truncates the text and adds an ellipses to the text.




## -see-also




<a href="https://msdn.microsoft.com/b14ddc05-7e7b-4fc6-b7e3-efe892df7e21">GetStockObject</a>



<a href="https://msdn.microsoft.com/619a6f21-fbac-455c-a702-0302ce13112b">ITfLangBarItemBalloon</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a>
 

 

