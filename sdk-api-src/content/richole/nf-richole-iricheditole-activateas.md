---
UID: NF:richole.IRichEditOle.ActivateAs
title: IRichEditOle::ActivateAs (richole.h)
description: Handles Activate As behavior by unloading all objects of the old class, telling OLE to treat those objects as objects of the new class, and reloading the objects. If objects cannot be reloaded, they are deleted.
helpviewer_keywords: ["ActivateAs","ActivateAs method [Windows Controls]","ActivateAs method [Windows Controls]","IRichEditOle interface","IRichEditOle interface [Windows Controls]","ActivateAs method","IRichEditOle.ActivateAs","IRichEditOle::ActivateAs","_win32_IRichEditOle_ActivateAs","_win32_IRichEditOle_ActivateAs_cpp","controls.IRichEditOle_ActivateAs","controls._win32_IRichEditOle_ActivateAs","richole/IRichEditOle::ActivateAs"]
old-location: controls\IRichEditOle_ActivateAs.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditoleactivateas.htm
ms.date: 12/05/2018
ms.keywords: ActivateAs, ActivateAs method [Windows Controls], ActivateAs method [Windows Controls],IRichEditOle interface, IRichEditOle interface [Windows Controls],ActivateAs method, IRichEditOle.ActivateAs, IRichEditOle::ActivateAs, _win32_IRichEditOle_ActivateAs, _win32_IRichEditOle_ActivateAs_cpp, controls.IRichEditOle_ActivateAs, controls._win32_IRichEditOle_ActivateAs, richole/IRichEditOle::ActivateAs
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
 - IRichEditOle::ActivateAs
 - richole/IRichEditOle::ActivateAs
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
 - IRichEditOle.ActivateAs
---

# IRichEditOle::ActivateAs


## -description

Handles <b>Activate As</b> behavior by unloading all objects of the old class, telling OLE to treat those objects as objects of the new class, and reloading the objects. If objects cannot be reloaded, they are deleted.

## -parameters

### -param rclsid

Type: <b>REFCLSID</b>

Class identifier of the old class.

### -param rclsidAs

Type: <b>REFCLSID</b>

Class identifier of the new class.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise.

## -see-also

<a href="/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a>