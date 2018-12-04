---
UID: NF:msctf.ITfContextOwnerServices.OnLayoutChange
title: ITfContextOwnerServices::OnLayoutChange
author: windows-sdk-content
description: The ITfContextOwnerServices::OnLayoutChange method is called by the context owner when the on-screen representation of the text stream is updated during a composition.
old-location: tsf\itfcontextownerservices_onlayoutchange.htm
tech.root: TSF
ms.assetid: a9e17687-6be6-4d2d-ba3a-6c128e71de26
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ITfContextOwnerServices interface [Text Services Framework],OnLayoutChange method, ITfContextOwnerServices.OnLayoutChange, ITfContextOwnerServices::OnLayoutChange, OnLayoutChange, OnLayoutChange method [Text Services Framework], OnLayoutChange method [Text Services Framework],ITfContextOwnerServices interface, _tsf_itfcontextownerservices_onlayoutchange_ref, msctf/ITfContextOwnerServices::OnLayoutChange, tsf.itfcontextownerservices_onlayoutchange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ITfContextOwnerServices.OnLayoutChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfContextOwnerServices::OnLayoutChange


## -description


The <b>ITfContextOwnerServices::OnLayoutChange</b> method is called by the context owner when the on-screen representation of the text stream is updated during a composition. Text stream updates include when the position of the window that contains the text is changed or if the screen coordinates of the text change.


## -parameters






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



A call to <b>ITfContextOwnerServices::OnLayoutChange</b> could be in response to a text edit, font size change, window movement/resizing, and so on.

If a call to <a href="https://msdn.microsoft.com/d621e96b-d357-4468-8a89-89445fb1ca9e">ITfContextView::GetTextExt</a> or <a href="https://msdn.microsoft.com/b6489391-a19e-405a-a129-f68054088860">ITfContextOwner::GetACPFromPoint</a> fails because the application did not calculate the screen layout (Return Value: TS_E_NOLAYOUT), the application must then call <b>ITfContextOwnerServices::OnLayoutChange</b> when the information is ready.




## -see-also




<a href="https://msdn.microsoft.com/b6489391-a19e-405a-a129-f68054088860">ITfContextOwner::GetACPFromPoint
      </a>



<a href="https://msdn.microsoft.com/fb77bd6a-ae34-4e21-8f09-fc8c6a1ade86">ITfContextOwnerServices</a>



<a href="https://msdn.microsoft.com/d621e96b-d357-4468-8a89-89445fb1ca9e">ITfContextView::GetTextExt
      </a>
 

 

