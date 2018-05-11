---
UID: NF:msctf.ITfContextView.GetScreenExt
title: ITfContextView::GetScreenExt
author: windows-driver-content
description: The ITfContextView::GetScreenExt method returns the bounding box, in screen coordinates, of the document display.
old-location: tsf\itfcontextview_getscreenext.htm
old-project: TSF
ms.assetid: 86dde611-4c46-418c-aa89-728081a28943
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetScreenExt, GetScreenExt method [Text Services Framework], GetScreenExt method [Text Services Framework],ITfContextView interface, ITfContextView interface [Text Services Framework],GetScreenExt method, ITfContextView.GetScreenExt, ITfContextView::GetScreenExt, _tsf_itfcontextview_getscreenext_ref, msctf/ITfContextView::GetScreenExt, tsf.itfcontextview_getscreenext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfContextView.GetScreenExt
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContextView::GetScreenExt


## -description


The <b>ITfContextView::GetScreenExt</b> method returns the bounding box, in screen coordinates, of the document display.


## -parameters




### -param prc [out]

Receives the bounding box, in screen coordinates, of the display surface.


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



The <i>prc</i> parameter is cleared to {0,0,0,0} if the document is not currently displayed.




## -see-also




<a href="https://msdn.microsoft.com/bd542dd1-79a5-47ec-a563-cd37a8c36b1a">
        ITextStoreACP::GetScreenExt
      </a>



<a href="https://msdn.microsoft.com/499a446d-1575-4636-b444-dd6078ed8736">ITfContextOwner::GetScreenExt
      </a>



<a href="https://msdn.microsoft.com/302d185d-dab7-4a77-a5cf-da2529d8b24a">ITfContextView</a>



<a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">
        TsViewCookie
      </a>
 

 

