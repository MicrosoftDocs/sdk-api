---
UID: NN:msctf.ITfContextOwner
title: ITfContextOwner (msctf.h)
author: windows-sdk-content
description: The ITfContextOwner interface is implemented by an application or a text service to receive text input without having a text store. An instance of this interface is obtained when the application calls the ITfSource::AdviseSink method.
old-location: tsf\itfcontextowner.htm
tech.root: TSF
ms.assetid: 630646df-dd47-4dbf-9787-f9d697ad8d7a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfContextOwner, ITfContextOwner interface [Text Services Framework], ITfContextOwner interface [Text Services Framework],described, _tsf_itfcontextowner_ref, msctf/ITfContextOwner, tsf.itfcontextowner
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
ms.custom: 19H1
---

# ITfContextOwner interface


## -description


The <b>ITfContextOwner</b> interface is implemented by an application or a text service to receive text input without having a text store. An instance of this interface is obtained when the application calls the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfContextOwner</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfContextOwner</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getacpfrompoint">GetACPFromPoint</a>
</td>
<td align="left" width="63%">
Converts a point, in screen coordinates, to an application character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getattribute">GetAttribute</a>
</td>
<td align="left" width="63%">
Returns the value of a supported attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getscreenext">GetScreenExt</a>
</td>
<td align="left" width="63%">
Returns the bounding box, in screen coordinates, of the display surface where the text stream is rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Obtains the status of a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextowner-gettextext">GetTextExt</a>
</td>
<td align="left" width="63%">
Returns the bounding box, in screen coordinates, of the text at a specified character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getwnd">GetWnd</a>
</td>
<td align="left" width="63%">
Returns the handle to a window that corresponds to the current document.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

