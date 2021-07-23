---
UID: NF:shlobj.IDocViewSite.OnSetTitle
title: IDocViewSite::OnSetTitle (shlobj.h)
description: Sets or retrieves the title of the site object.
helpviewer_keywords: ["IDocViewSite interface [Windows Shell]","OnSetTitle method","IDocViewSite.OnSetTitle","IDocViewSite::OnSetTitle","OnSetTitle","OnSetTitle method [Windows Shell]","OnSetTitle method [Windows Shell]","IDocViewSite interface","_win32_IDocViewSite_OnSetTitle","shell.IDocViewSite_OnSetTitle","shlobj/IDocViewSite::OnSetTitle"]
old-location: shell\IDocViewSite_OnSetTitle.htm
tech.root: shell
ms.assetid: 941a8fe0-27db-4646-97d0-287fc94e7721
ms.date: 12/05/2018
ms.keywords: IDocViewSite interface [Windows Shell],OnSetTitle method, IDocViewSite.OnSetTitle, IDocViewSite::OnSetTitle, OnSetTitle, OnSetTitle method [Windows Shell], OnSetTitle method [Windows Shell],IDocViewSite interface, _win32_IDocViewSite_OnSetTitle, shell.IDocViewSite_OnSetTitle, shlobj/IDocViewSite::OnSetTitle
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDocViewSite::OnSetTitle
 - shlobj/IDocViewSite::OnSetTitle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDocViewSite.OnSetTitle
---

# IDocViewSite::OnSetTitle


## -description

Sets or retrieves the title of the site object.

## -parameters

### -param pvTitle [in]

Type: <b>VARIANTARG*</b>

Specifies the view title.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

