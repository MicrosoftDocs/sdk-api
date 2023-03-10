---
UID: NF:richole.IRichEditOle.ContextSensitiveHelp
title: IRichEditOle::ContextSensitiveHelp (richole.h)
description: Indicates if a rich edit control should transition into or out of context-sensitive help mode. A rich edit control calls the IRichEditOle::ContextSensitiveHelp method of any in-place object which is currently active if a state change is occurring.
helpviewer_keywords: ["ContextSensitiveHelp","ContextSensitiveHelp method [Windows Controls]","ContextSensitiveHelp method [Windows Controls]","IRichEditOle interface","IRichEditOle interface [Windows Controls]","ContextSensitiveHelp method","IRichEditOle.ContextSensitiveHelp","IRichEditOle::ContextSensitiveHelp","_win32_IRichEditOle_ContextSensitiveHelp","_win32_IRichEditOle_ContextSensitiveHelp_cpp","controls.IRichEditOle_ContextSensitiveHelp","controls._win32_IRichEditOle_ContextSensitiveHelp","richole/IRichEditOle::ContextSensitiveHelp"]
old-location: controls\IRichEditOle_ContextSensitiveHelp.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditolecontextsensitivehelp.htm
ms.date: 12/05/2018
ms.keywords: ContextSensitiveHelp, ContextSensitiveHelp method [Windows Controls], ContextSensitiveHelp method [Windows Controls],IRichEditOle interface, IRichEditOle interface [Windows Controls],ContextSensitiveHelp method, IRichEditOle.ContextSensitiveHelp, IRichEditOle::ContextSensitiveHelp, _win32_IRichEditOle_ContextSensitiveHelp, _win32_IRichEditOle_ContextSensitiveHelp_cpp, controls.IRichEditOle_ContextSensitiveHelp, controls._win32_IRichEditOle_ContextSensitiveHelp, richole/IRichEditOle::ContextSensitiveHelp
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
 - IRichEditOle::ContextSensitiveHelp
 - richole/IRichEditOle::ContextSensitiveHelp
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
 - IRichEditOle.ContextSensitiveHelp
---

# IRichEditOle::ContextSensitiveHelp


## -description

Indicates if a rich edit control should transition into or out of context-sensitive help mode. A rich edit control calls the <b>IRichEditOle::ContextSensitiveHelp</b> method of any in-place object which is currently active if a state change is occurring.

## -parameters

### -param fEnterMode

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Indicator of whether the control is entering context-sensitive help mode (<b>TRUE</b>) or leaving it (<b>FALSE</b>).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise.

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a>