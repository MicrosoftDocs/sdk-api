---
UID: NF:shldisp.IAutoComplete2.GetOptions
title: IAutoComplete2::GetOptions (shldisp.h)
description: Gets the current autocomplete options. (IAutoComplete2.GetOptions)
helpviewer_keywords: ["GetOptions","GetOptions method [Windows Shell]","GetOptions method [Windows Shell]","IAutoComplete2 interface","IAutoComplete2 interface [Windows Shell]","GetOptions method","IAutoComplete2.GetOptions","IAutoComplete2::GetOptions","_win32_IAutoComplete2_GetOptions","shell.IAutoComplete2_GetOptions","shldisp/IAutoComplete2::GetOptions"]
old-location: shell\IAutoComplete2_GetOptions.htm
tech.root: shell
ms.assetid: 00c2aa5f-eebc-479c-ac33-6efb3acb1051
ms.date: 12/05/2018
ms.keywords: GetOptions, GetOptions method [Windows Shell], GetOptions method [Windows Shell],IAutoComplete2 interface, IAutoComplete2 interface [Windows Shell],GetOptions method, IAutoComplete2.GetOptions, IAutoComplete2::GetOptions, _win32_IAutoComplete2_GetOptions, shell.IAutoComplete2_GetOptions, shldisp/IAutoComplete2::GetOptions
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAutoComplete2::GetOptions
 - shldisp/IAutoComplete2::GetOptions
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
 - IAutoComplete2.GetOptions
---

# IAutoComplete2::GetOptions


## -description

Gets the current autocomplete options.

## -parameters

### -param pdwFlag [out]

Type: <b>DWORD*</b>

One or more flags from the <a href="/windows/desktop/api/shldisp/ne-shldisp-autocompleteoptions">AUTOCOMPLETEOPTIONS</a> enumeration that indicate the options that are currently set.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-iautocomplete2">IAutoComplete2</a>



<a href="/windows/desktop/api/shldisp/nf-shldisp-iautocomplete2-setoptions">IAutoComplete2::SetOptions</a>
