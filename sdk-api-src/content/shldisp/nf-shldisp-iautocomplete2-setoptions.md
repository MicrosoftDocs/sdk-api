---
UID: NF:shldisp.IAutoComplete2.SetOptions
title: IAutoComplete2::SetOptions (shldisp.h)
description: Sets the current autocomplete options. (IAutoComplete2.SetOptions)
helpviewer_keywords: ["IAutoComplete2 interface [Windows Shell]","SetOptions method","IAutoComplete2.SetOptions","IAutoComplete2::SetOptions","SetOptions","SetOptions method [Windows Shell]","SetOptions method [Windows Shell]","IAutoComplete2 interface","_win32_IAutoComplete2_SetOptions","shell.IAutoComplete2_SetOptions","shldisp/IAutoComplete2::SetOptions"]
old-location: shell\IAutoComplete2_SetOptions.htm
tech.root: shell
ms.assetid: d3562845-fc28-4726-a520-29720f9924fc
ms.date: 12/05/2018
ms.keywords: IAutoComplete2 interface [Windows Shell],SetOptions method, IAutoComplete2.SetOptions, IAutoComplete2::SetOptions, SetOptions, SetOptions method [Windows Shell], SetOptions method [Windows Shell],IAutoComplete2 interface, _win32_IAutoComplete2_SetOptions, shell.IAutoComplete2_SetOptions, shldisp/IAutoComplete2::SetOptions
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
 - IAutoComplete2::SetOptions
 - shldisp/IAutoComplete2::SetOptions
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
 - IAutoComplete2.SetOptions
---

# IAutoComplete2::SetOptions


## -description

Sets the current autocomplete options.

## -parameters

### -param dwFlag [in]

Type: <b>DWORD</b>

One or more flags from the <a href="/windows/desktop/api/shldisp/ne-shldisp-autocompleteoptions">AUTOCOMPLETEOPTIONS</a> enumeration that specify autocomplete options.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The TAB key is disabled by default because it is typically used to navigate from control to control, not within a control. If you set the <a href="/windows/desktop/api/shldisp/ne-shldisp-autocompleteoptions">ACO_USETAB</a> flag in <i>dwFlag</i>, users can navigate to a string in the drop-down list by pressing the TAB key. If the drop-down list is closed, the TAB key allows the user to navigate from control to control, as usual. The user can close the drop-down list by pressing the ESC key.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-iautocomplete2">IAutoComplete2</a>



<a href="/windows/desktop/api/shldisp/nf-shldisp-iautocomplete2-getoptions">IAutoComplete2::GetOptions</a>
