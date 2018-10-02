---
UID: NF:ctfutb.ITfLangBarItemBalloon.GetPreferredSize
title: ITfLangBarItemBalloon::GetPreferredSize
author: windows-sdk-content
description: ITfLangBarItemBalloon::GetPreferredSize method
old-location: tsf\itflangbaritemballoon_getpreferredsize.htm
tech.root: TSF
ms.assetid: 73f3a12e-b787-424e-9998-276baee63264
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetPreferredSize, GetPreferredSize method [Text Services Framework], GetPreferredSize method [Text Services Framework],ITfLangBarItemBalloon interface, ITfLangBarItemBalloon interface [Text Services Framework],GetPreferredSize method, ITfLangBarItemBalloon.GetPreferredSize, ITfLangBarItemBalloon::GetPreferredSize, _tsf_itflangbaritemballoon_getpreferredsize_ref, ctfutb/ITfLangBarItemBalloon::GetPreferredSize, tsf.itflangbaritemballoon_getpreferredsize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfLangBarItemBalloon.GetPreferredSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarItemBalloon::GetPreferredSize


## -description




## -parameters




### -param pszDefault [in]

Pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that contains the default size, in pixels, of the balloon.


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



<a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>
 

 

