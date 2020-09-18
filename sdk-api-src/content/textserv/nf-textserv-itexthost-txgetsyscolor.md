---
UID: NF:textserv.ITextHost.TxGetSysColor
title: ITextHost::TxGetSysColor (textserv.h)
description: Retrieves the text host's color for a specified display element.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxGetSysColor method","ITextHost.TxGetSysColor","ITextHost::TxGetSysColor","TxGetSysColor","TxGetSysColor method [Windows Controls]","TxGetSysColor method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxGetSysColor","_win32_ITextHost_TxGetSysColor_cpp","controls.ITextHost_TxGetSysColor","controls._win32_ITextHost_TxGetSysColor","textserv/ITextHost::TxGetSysColor"]
old-location: controls\ITextHost_TxGetSysColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxgetsyscolor.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetSysColor method, ITextHost.TxGetSysColor, ITextHost::TxGetSysColor, TxGetSysColor, TxGetSysColor method [Windows Controls], TxGetSysColor method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetSysColor, _win32_ITextHost_TxGetSysColor_cpp, controls.ITextHost_TxGetSysColor, controls._win32_ITextHost_TxGetSysColor, textserv/ITextHost::TxGetSysColor
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
 - ITextHost::TxGetSysColor
 - textserv/ITextHost::TxGetSysColor
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
 - ITextHost.TxGetSysColor
---

# ITextHost::TxGetSysColor


## -description

Retrieves the text host's color for a specified display element.

## -parameters

### -param nIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

The display element whose color is to be retrieved. For a list of possible values for this parameter, see the <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> function.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The  value that identifies the red, green, and blue (RGB) color value of the specified element.

## -remarks

Note that the color returned may be 
				<i>different</i> than the color that would be returned from a call to <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a>. This is the case if the host overrides the default system behavior.

<div class="alert"><b>Note</b>  Hosts should be careful about overriding normal system behavior because it can result in inconsistent UI (particularly with respect to Accessibility options).</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>