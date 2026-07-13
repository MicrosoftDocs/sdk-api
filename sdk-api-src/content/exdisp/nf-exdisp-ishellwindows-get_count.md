---
UID: NF:exdisp.IShellWindows.get_Count
title: IShellWindows::get_Count (exdisp.h)
description: Gets the number of windows in the Shell windows collection.
helpviewer_keywords: ["IShellWindows interface [Windows Shell]","get_Count method","IShellWindows.get_Count","IShellWindows::get_Count","_win32_IShellWindows_get_Count","exdisp/IShellWindows::get_Count","get_Count","get_Count method [Windows Shell]","get_Count method [Windows Shell]","IShellWindows interface","shell.IShellWindows_get_Count"]
old-location: shell\IShellWindows_get_Count.htm
tech.root: shell
ms.assetid: 50781569-4c80-4304-96f3-8a135cea3b20
ms.date: 12/05/2018
ms.keywords: IShellWindows interface [Windows Shell],get_Count method, IShellWindows.get_Count, IShellWindows::get_Count, _win32_IShellWindows_get_Count, exdisp/IShellWindows::get_Count, get_Count, get_Count method [Windows Shell], get_Count method [Windows Shell],IShellWindows interface, shell.IShellWindows_get_Count
req.header: exdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Exdisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shdocvw.dll (version 5.00.2014.0216 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5
ms.custom: 19H1
f1_keywords:
 - IShellWindows::get_Count
 - exdisp/IShellWindows::get_Count
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IShellWindows.get_Count
---

# IShellWindows::get_Count


## -description

Gets the number of windows in the Shell windows collection.

## -parameters

### -param Count [out, retval]

Type: <b>long*</b>

The number of windows in the Shell windows collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/exdisp/nn-exdisp-ishellwindows">IShellWindows</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-item">IShellWindows::Item</a>



<a href="/windows/win32/api/exdisp/nf-exdisp-ishellwindows-_newenum">IShellWindows::_NewEnum</a>