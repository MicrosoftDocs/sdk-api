---
UID: NF:ctfutb.ITfLangBarItemBitmapButton.GetPreferredSize
title: ITfLangBarItemBitmapButton::GetPreferredSize
author: windows-sdk-content
description: ITfLangBarItemBitmapButton::GetPreferredSize method
old-location: tsf\itflangbaritembitmapbutton_getpreferredsize.htm
tech.root: TSF
ms.assetid: 271e4e24-c81e-484c-84bb-d7b67038a5c5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetPreferredSize, GetPreferredSize method [Text Services Framework], GetPreferredSize method [Text Services Framework],ITfLangBarItemBitmapButton interface, ITfLangBarItemBitmapButton interface [Text Services Framework],GetPreferredSize method, ITfLangBarItemBitmapButton.GetPreferredSize, ITfLangBarItemBitmapButton::GetPreferredSize, _tsf_itflangbaritembitmapbutton_getpreferredsize_ref, ctfutb/ITfLangBarItemBitmapButton::GetPreferredSize, tsf.itflangbaritembitmapbutton_getpreferredsize
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
 - ITfLangBarItemBitmapButton.GetPreferredSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarItemBitmapButton::GetPreferredSize


## -description




## -parameters




### -param pszDefault [in]

Pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that contains the default size, in pixels, of the bitmap.


### -param psz [out]

Pointer to a SIZE structure that recevies the preferred size, in pixels, of the bitmap. The <b>cy</b> member of this structure is ignored.


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



The results of this method are not currently used. The bitmap for a bitmap button item should not be larger than the size of a small icon. Obtain these dimensions by calling <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> with SM_CXSMICON for the width and SM_CYSMICON for the height.




## -see-also




<a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>



<a href="https://msdn.microsoft.com/29fcc913-fcc7-4321-918b-2c354dd751ff">ITfLangBarItemBitmapButton</a>



<a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>
 

 

