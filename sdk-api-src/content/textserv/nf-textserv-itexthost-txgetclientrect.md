---
UID: NF:textserv.ITextHost.TxGetClientRect
title: ITextHost::TxGetClientRect (textserv.h)
description: Retrieves the client coordinates of the text host's client area.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxGetClientRect method","ITextHost.TxGetClientRect","ITextHost::TxGetClientRect","TxGetClientRect","TxGetClientRect method [Windows Controls]","TxGetClientRect method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxGetClientRect","_win32_ITextHost_TxGetClientRect_cpp","controls.ITextHost_TxGetClientRect","controls._win32_ITextHost_TxGetClientRect","textserv/ITextHost::TxGetClientRect"]
old-location: controls\ITextHost_TxGetClientRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetclientrect.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetClientRect method, ITextHost.TxGetClientRect, ITextHost::TxGetClientRect, TxGetClientRect, TxGetClientRect method [Windows Controls], TxGetClientRect method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetClientRect, _win32_ITextHost_TxGetClientRect_cpp, controls.ITextHost_TxGetClientRect, controls._win32_ITextHost_TxGetClientRect, textserv/ITextHost::TxGetClientRect
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextHost::TxGetClientRect
 - textserv/ITextHost::TxGetClientRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextHost.TxGetClientRect
---

# ITextHost::TxGetClientRect


## -description

Retrieves the client coordinates of the text host's client area.

## -parameters

### -param prc

Type: <b>LPRECT</b>

The client coordinates of the text host's client area.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Return S_OK if the method succeeds. 

Return the following COM error code if the method fails. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
</table>

## -remarks

The client rectangle is the rectangle that the text services object is responsible for painting and managing. The host relies on the text services object for painting that area. And, the text services object must not paint or invalidate areas outside of that rectangle.

The host forwards mouse messages to the text services object when the cursor is over the client rectangle.

The client rectangle is expressed in client coordinates of the containing window.

<div class="alert"><b>Important</b>  The <b>ITextHost::TxGetClientRect</b> method will fail if called at an inactive time.</div>
<div> </div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>