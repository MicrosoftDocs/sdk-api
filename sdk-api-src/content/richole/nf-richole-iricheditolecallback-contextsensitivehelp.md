---
UID: NF:richole.IRichEditOleCallback.ContextSensitiveHelp
title: IRichEditOleCallback::ContextSensitiveHelp (richole.h)
description: Indicates if the application should transition into or out of context-sensitive help mode. This method should implement the functionality described for IOleWindow::ContextSensitiveHelp.
helpviewer_keywords: ["ContextSensitiveHelp","ContextSensitiveHelp method [Windows Controls]","ContextSensitiveHelp method [Windows Controls]","IRichEditOleCallback interface","IRichEditOleCallback interface [Windows Controls]","ContextSensitiveHelp method","IRichEditOleCallback.ContextSensitiveHelp","IRichEditOleCallback::ContextSensitiveHelp","_win32_IRichEditOleCallback_ContextSensitiveHelp","_win32_IRichEditOleCallback_ContextSensitiveHelp_cpp","controls.IRichEditOleCallback_ContextSensitiveHelp","controls._win32_IRichEditOleCallback_ContextSensitiveHelp","richole/IRichEditOleCallback::ContextSensitiveHelp"]
old-location: controls\IRichEditOleCallback_ContextSensitiveHelp.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback\iricheditolecallbackcontextsensitivehelp.htm
ms.date: 12/05/2018
ms.keywords: ContextSensitiveHelp, ContextSensitiveHelp method [Windows Controls], ContextSensitiveHelp method [Windows Controls],IRichEditOleCallback interface, IRichEditOleCallback interface [Windows Controls],ContextSensitiveHelp method, IRichEditOleCallback.ContextSensitiveHelp, IRichEditOleCallback::ContextSensitiveHelp, _win32_IRichEditOleCallback_ContextSensitiveHelp, _win32_IRichEditOleCallback_ContextSensitiveHelp_cpp, controls.IRichEditOleCallback_ContextSensitiveHelp, controls._win32_IRichEditOleCallback_ContextSensitiveHelp, richole/IRichEditOleCallback::ContextSensitiveHelp
req.header: richole.h
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
 - IRichEditOleCallback::ContextSensitiveHelp
 - richole/IRichEditOleCallback::ContextSensitiveHelp
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
 - IRichEditOleCallback.ContextSensitiveHelp
---

# IRichEditOleCallback::ContextSensitiveHelp


## -description

Indicates if the application should transition into or out of context-sensitive help mode. This method should implement the functionality described for <a href="/windows/desktop/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp">IOleWindow::ContextSensitiveHelp</a>.

## -parameters

### -param fEnterMode

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If <b>TRUE</b>, the application should enter context-sensitive help mode. If <b>FALSE</b>, the application should leave context-sensitive help mode.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns <b>S_OK</b> on success. If the method fails, it can be the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
There was an invalid argument.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditolecallback">IRichEditOleCallback</a>