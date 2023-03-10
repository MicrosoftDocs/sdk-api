---
UID: NF:textserv.ITextHost.TxGetExtent
title: ITextHost::TxGetExtent (textserv.h)
description: Requests the native size of the control in HIMETRIC.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxGetExtent method","ITextHost.TxGetExtent","ITextHost::TxGetExtent","TxGetExtent","TxGetExtent method [Windows Controls]","TxGetExtent method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxGetExtent","_win32_ITextHost_TxGetExtent_cpp","controls.ITextHost_TxGetExtent","controls._win32_ITextHost_TxGetExtent","textserv/ITextHost::TxGetExtent"]
old-location: controls\ITextHost_TxGetExtent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetextent.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetExtent method, ITextHost.TxGetExtent, ITextHost::TxGetExtent, TxGetExtent, TxGetExtent method [Windows Controls], TxGetExtent method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetExtent, _win32_ITextHost_TxGetExtent_cpp, controls.ITextHost_TxGetExtent, controls._win32_ITextHost_TxGetExtent, textserv/ITextHost::TxGetExtent
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
 - ITextHost::TxGetExtent
 - textserv/ITextHost::TxGetExtent
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
 - ITextHost.TxGetExtent
---

# ITextHost::TxGetExtent


## -description

Requests the native size of the control in HIMETRIC.

## -parameters

### -param lpExtent

Type: <b>LPSIZEL</b>

The size of the control in HIMETRIC, that is, where the unit is .01 millimeter.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented. 

</td>
</tr>
</table>

## -remarks

This method is used by the text services object to implement zooming. The text services object derives the zoom factor from the ratio between the himetric and device pixel extent of the client rectangle. Each HIMETRIC unit corresponds to 0.01 millimeter.

[vertical zoom factor] = [pixel height of the client rect] * 2540 / [HIMETRIC vertical extent] * [pixel per vertical inch (from device context)]

If the vertical and horizontal zoom factors are not the same, the text services object can ignore the horizontal zoom factor and assume it is the same as the vertical one.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Other Resources</b>



<a href="/windows/win32/api/windef/ns-windef-size">SIZE</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>