---
UID: NF:richole.IRichEditOle.HandsOffStorage
title: IRichEditOle::HandsOffStorage (richole.h)
description: Indicates when a rich edit control is to release its reference to the storage interface associated with the specified object. This call does not call the object's IRichEditOle::HandsOffStorage method; the caller must do that.
helpviewer_keywords: ["HandsOffStorage","HandsOffStorage method [Windows Controls]","HandsOffStorage method [Windows Controls]","IRichEditOle interface","IRichEditOle interface [Windows Controls]","HandsOffStorage method","IRichEditOle.HandsOffStorage","IRichEditOle::HandsOffStorage","_win32_IRichEditOle_HandsOffStorage","_win32_IRichEditOle_HandsOffStorage_cpp","controls.IRichEditOle_HandsOffStorage","controls._win32_IRichEditOle_HandsOffStorage","richole/IRichEditOle::HandsOffStorage"]
old-location: controls\IRichEditOle_HandsOffStorage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditolehandsoffstorage.htm
ms.date: 12/05/2018
ms.keywords: HandsOffStorage, HandsOffStorage method [Windows Controls], HandsOffStorage method [Windows Controls],IRichEditOle interface, IRichEditOle interface [Windows Controls],HandsOffStorage method, IRichEditOle.HandsOffStorage, IRichEditOle::HandsOffStorage, _win32_IRichEditOle_HandsOffStorage, _win32_IRichEditOle_HandsOffStorage_cpp, controls.IRichEditOle_HandsOffStorage, controls._win32_IRichEditOle_HandsOffStorage, richole/IRichEditOle::HandsOffStorage
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
 - IRichEditOle::HandsOffStorage
 - richole/IRichEditOle::HandsOffStorage
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
 - IRichEditOle.HandsOffStorage
---

# IRichEditOle::HandsOffStorage


## -description

Indicates when a rich edit control is to release its reference to the storage interface associated with the specified object. This call does not call the object's <b>IRichEditOle::HandsOffStorage</b> method; the caller must do that.

## -parameters

### -param iob

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Index of the object whose storage is to be released. If this parameter is REO_IOB_SELECTION, the storage of the selected object is to be released.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise. E_INVALIDARG is returned if the index is invalid.

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a>