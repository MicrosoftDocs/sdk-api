---
UID: NF:richole.IRichEditOle.SetDvaspect
title: IRichEditOle::SetDvaspect (richole.h)
description: Sets the aspect that a rich edit control uses to draw an object. This call does not change the drawing information cached in the object; this must be done by the caller. The call does cause the object to be redrawn.
helpviewer_keywords: ["IRichEditOle interface [Windows Controls]","SetDvaspect method","IRichEditOle.SetDvaspect","IRichEditOle::SetDvaspect","SetDvaspect","SetDvaspect method [Windows Controls]","SetDvaspect method [Windows Controls]","IRichEditOle interface","_win32_IRichEditOle_SetDvaspect","_win32_IRichEditOle_SetDvaspect_cpp","controls.IRichEditOle_SetDvaspect","controls._win32_IRichEditOle_SetDvaspect","richole/IRichEditOle::SetDvaspect"]
old-location: controls\IRichEditOle_SetDvaspect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditolesetdvaspect.htm
ms.date: 12/05/2018
ms.keywords: IRichEditOle interface [Windows Controls],SetDvaspect method, IRichEditOle.SetDvaspect, IRichEditOle::SetDvaspect, SetDvaspect, SetDvaspect method [Windows Controls], SetDvaspect method [Windows Controls],IRichEditOle interface, _win32_IRichEditOle_SetDvaspect, _win32_IRichEditOle_SetDvaspect_cpp, controls.IRichEditOle_SetDvaspect, controls._win32_IRichEditOle_SetDvaspect, richole/IRichEditOle::SetDvaspect
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
 - IRichEditOle::SetDvaspect
 - richole/IRichEditOle::SetDvaspect
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
 - IRichEditOle.SetDvaspect
---

# IRichEditOle::SetDvaspect


## -description

Sets the aspect that a rich edit control uses to draw an object. This call does not change the drawing information cached in the object; this must be done by the caller. The call does cause the object to be redrawn.

## -parameters

### -param iob

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Index of the object whose aspect is to be set. If this parameter is REO_IOB_SELECTION, the aspect of the selected object is to be set.

### -param dvaspect

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Aspect to use when drawing. The values are defined by OLE.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise. E_INVALIDARG is returned if the index is invalid.

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a>