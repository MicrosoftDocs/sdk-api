---
UID: NF:msctf.ITfContextOwner.GetScreenExt
title: ITfContextOwner::GetScreenExt
author: windows-sdk-content
description: The ITfContextOwner::GetScreenExt method returns the bounding box, in screen coordinates, of the display surface where the text stream is rendered.
old-location: tsf\itfcontextowner_getscreenext.htm
tech.root: TSF
ms.assetid: 499a446d-1575-4636-b444-dd6078ed8736
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetScreenExt, GetScreenExt method [Text Services Framework], GetScreenExt method [Text Services Framework],ITfContextOwner interface, ITfContextOwner interface [Text Services Framework],GetScreenExt method, ITfContextOwner.GetScreenExt, ITfContextOwner::GetScreenExt, _tsf_itfcontextowner_getscreenext_ref, msctf/ITfContextOwner::GetScreenExt, tsf.itfcontextowner_getscreenext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msimtf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msimtf.dll
api_name:
 - ITfContextOwner.GetScreenExt
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- msctf.h
: 
- ITfContextOwner.GetScreenExt
: 
---

# ITfContextOwner::GetScreenExt


## -description


The <b>ITfContextOwner::GetScreenExt</b> method returns the bounding box, in screen coordinates, of the display surface where the text stream is rendered.


## -parameters




### -param prc [out]

Receives the bounding box screen coordinates of the display surface of the document.


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



If the text is not currently displayed, for example if the document window is minimized, <i>prc</i> is set to { 0, 0, 0, 0 }.




## -see-also




<a href="https://msdn.microsoft.com/bd542dd1-79a5-47ec-a563-cd37a8c36b1a">ITextStoreACP::GetScreenExt
      </a>



<a href="https://msdn.microsoft.com/630646df-dd47-4dbf-9787-f9d697ad8d7a">ITfContextOwner</a>



<a href="https://msdn.microsoft.com/86dde611-4c46-418c-aa89-728081a28943">ITfContextView::GetScreenExt
      </a>



<a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">TsViewCookie
      </a>
 

 

