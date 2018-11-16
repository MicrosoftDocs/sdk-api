---
UID: NN:msctf.ITfContextOwner
title: ITfContextOwner
author: windows-sdk-content
description: The ITfContextOwner interface is implemented by an application or a text service to receive text input without having a text store. An instance of this interface is obtained when the application calls the ITfSource::AdviseSink method.
old-location: tsf\itfcontextowner.htm
tech.root: TSF
ms.assetid: 630646df-dd47-4dbf-9787-f9d697ad8d7a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITfContextOwner, ITfContextOwner interface [Text Services Framework], ITfContextOwner interface [Text Services Framework],described, _tsf_itfcontextowner_ref, msctf/ITfContextOwner, tsf.itfcontextowner
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ITfContextOwner
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfContextOwner interface


## -description


The <b>ITfContextOwner</b> interface is implemented by an application or a text service to receive text input without having a text store. An instance of this interface is obtained when the application calls the <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfContextOwner</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfContextOwner</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfContextOwner</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8091e79-33af-49d5-b3c8-d30952c62010">GetACPFromPoint</a>
</td>
<td align="left" width="63%">
Converts a point, in screen coordinates, to an application character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a249d529-fdb1-4f5f-84ae-f26dae917609">GetAttribute</a>
</td>
<td align="left" width="63%">
Returns the value of a supported attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/499a446d-1575-4636-b444-dd6078ed8736">GetScreenExt</a>
</td>
<td align="left" width="63%">
Returns the bounding box, in screen coordinates, of the display surface where the text stream is rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce30ec8a-48fe-4ec7-a7e1-2a0cf084097d">GetStatus</a>
</td>
<td align="left" width="63%">
Obtains the status of a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/edde0ba7-1d88-4c32-b794-761b66d73507">GetTextExt</a>
</td>
<td align="left" width="63%">
Returns the bounding box, in screen coordinates, of the text at a specified character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91dfc873-3327-49f4-924a-b013fa90459b">GetWnd</a>
</td>
<td align="left" width="63%">
Returns the handle to a window that corresponds to the current document.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

