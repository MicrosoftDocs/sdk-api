---
UID: NF:ctfutb.ITfLangBarItemBitmap.GetPreferredSize
title: ITfLangBarItemBitmap::GetPreferredSize
author: windows-sdk-content
description: ITfLangBarItemBitmap::GetPreferredSize method
old-location: tsf\itflangbaritembitmap_getpreferredsize.htm
tech.root: TSF
ms.assetid: 4dd173de-6b54-4d03-b458-0dd5186d1d83
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetPreferredSize, GetPreferredSize method [Text Services Framework], GetPreferredSize method [Text Services Framework],ITfLangBarItemBitmap interface, ITfLangBarItemBitmap interface [Text Services Framework],GetPreferredSize method, ITfLangBarItemBitmap.GetPreferredSize, ITfLangBarItemBitmap::GetPreferredSize, _tsf_itflangbaritembitmap_getpreferredsize_ref, ctfutb/ITfLangBarItemBitmap::GetPreferredSize, tsf.itflangbaritembitmap_getpreferredsize
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
 - ITfLangBarItemBitmap.GetPreferredSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarItemBitmap::GetPreferredSize


## -description




## -parameters




### -param pszDefault [in]

Pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that contains the default size, in pixels, of the bitmap.


### -param psz [out]

Pointer to a <b>SIZE</b> structure that receives the preferred size, in pixels, of the bitmap. The <b>cy</b> member of this structure is ignored.


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
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms628706(v=VS.85).aspx">ITfLangBarItemBitmap</a>



<a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>
 

 

