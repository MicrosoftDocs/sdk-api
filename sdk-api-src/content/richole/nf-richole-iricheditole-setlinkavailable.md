---
UID: NF:richole.IRichEditOle.SetLinkAvailable
title: IRichEditOle::SetLinkAvailable (richole.h)
description: Sets the value of the link-available bit in the object's flags.
helpviewer_keywords: ["IRichEditOle interface [Windows Controls]","SetLinkAvailable method","IRichEditOle.SetLinkAvailable","IRichEditOle::SetLinkAvailable","SetLinkAvailable","SetLinkAvailable method [Windows Controls]","SetLinkAvailable method [Windows Controls]","IRichEditOle interface","_win32_IRichEditOle_SetLinkAvailable","_win32_IRichEditOle_SetLinkAvailable_cpp","controls.IRichEditOle_SetLinkAvailable","controls._win32_IRichEditOle_SetLinkAvailable","richole/IRichEditOle::SetLinkAvailable"]
old-location: controls\IRichEditOle_SetLinkAvailable.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditolesetlinkavailable.htm
ms.date: 12/05/2018
ms.keywords: IRichEditOle interface [Windows Controls],SetLinkAvailable method, IRichEditOle.SetLinkAvailable, IRichEditOle::SetLinkAvailable, SetLinkAvailable, SetLinkAvailable method [Windows Controls], SetLinkAvailable method [Windows Controls],IRichEditOle interface, _win32_IRichEditOle_SetLinkAvailable, _win32_IRichEditOle_SetLinkAvailable_cpp, controls.IRichEditOle_SetLinkAvailable, controls._win32_IRichEditOle_SetLinkAvailable, richole/IRichEditOle::SetLinkAvailable
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
 - IRichEditOle::SetLinkAvailable
 - richole/IRichEditOle::SetLinkAvailable
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
 - IRichEditOle.SetLinkAvailable
---

# IRichEditOle::SetLinkAvailable


## -description

Sets the value of the link-available bit in the object's flags. The link-available bit defaults to <b>TRUE</b>. It should be set to <b>FALSE</b> if any errors occur on the link which would indicate problems connecting to the linked object or application. When those problems are repaired, the bit should be set to <b>TRUE</b> again.

## -parameters

### -param iob

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Index of object whose bit is to be set. If this parameter is REO_IOB_SELECTION, the bit on the selected object is to be set.

### -param fAvailable

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Value used in the set operation. The value can be <b>TRUE</b> or <b>FALSE</b>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise. E_INVALIDARG is returned if the index is invalid.

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a>