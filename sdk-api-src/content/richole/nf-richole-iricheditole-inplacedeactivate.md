---
UID: NF:richole.IRichEditOle.InPlaceDeactivate
title: IRichEditOle::InPlaceDeactivate (richole.h)
description: Indicates when a rich edit control is to deactivate the currently active in-place object, if any.
helpviewer_keywords: ["IRichEditOle interface [Windows Controls]","InPlaceDeactivate method","IRichEditOle.InPlaceDeactivate","IRichEditOle::InPlaceDeactivate","InPlaceDeactivate","InPlaceDeactivate method [Windows Controls]","InPlaceDeactivate method [Windows Controls]","IRichEditOle interface","_win32_IRichEditOle_InPlaceDeactivate","_win32_IRichEditOle_InPlaceDeactivate_cpp","controls.IRichEditOle_InPlaceDeactivate","controls._win32_IRichEditOle_InPlaceDeactivate","richole/IRichEditOle::InPlaceDeactivate"]
old-location: controls\IRichEditOle_InPlaceDeactivate.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditoleinplacedeactivate.htm
ms.date: 12/05/2018
ms.keywords: IRichEditOle interface [Windows Controls],InPlaceDeactivate method, IRichEditOle.InPlaceDeactivate, IRichEditOle::InPlaceDeactivate, InPlaceDeactivate, InPlaceDeactivate method [Windows Controls], InPlaceDeactivate method [Windows Controls],IRichEditOle interface, _win32_IRichEditOle_InPlaceDeactivate, _win32_IRichEditOle_InPlaceDeactivate_cpp, controls.IRichEditOle_InPlaceDeactivate, controls._win32_IRichEditOle_InPlaceDeactivate, richole/IRichEditOle::InPlaceDeactivate
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
 - IRichEditOle::InPlaceDeactivate
 - richole/IRichEditOle::InPlaceDeactivate
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
 - IRichEditOle.InPlaceDeactivate
---

# IRichEditOle::InPlaceDeactivate


## -description

Indicates when a rich edit control is to deactivate the currently active in-place object, if any.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise. If there is no active in-place object, the method succeeds.

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a>
