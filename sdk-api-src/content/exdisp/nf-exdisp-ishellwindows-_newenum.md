---
UID: NF:exdisp.IShellWindows._NewEnum
title: IShellWindows::_NewEnum (exdisp.h)
description: Retrieves an enumerator for the collection of Shell windows.
helpviewer_keywords: ["IShellWindows interface [Windows Shell]","_NewEnum method","IShellWindows._NewEnum","IShellWindows::_NewEnum","_NewEnum","_NewEnum method [Windows Shell]","_NewEnum method [Windows Shell]","IShellWindows interface","_win32_IShellWindows_NewEnum","exdisp/IShellWindows::_NewEnum","shell.IShellWindows_NewEnum"]
old-location: shell\IShellWindows_NewEnum.htm
tech.root: shell
ms.assetid: e91b2be7-2be9-4460-9a2a-57090dcfc961
ms.date: 12/05/2018
ms.keywords: IShellWindows interface [Windows Shell],_NewEnum method, IShellWindows._NewEnum, IShellWindows::_NewEnum, _NewEnum, _NewEnum method [Windows Shell], _NewEnum method [Windows Shell],IShellWindows interface, _win32_IShellWindows_NewEnum, exdisp/IShellWindows::_NewEnum, shell.IShellWindows_NewEnum
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
 - IShellWindows::_NewEnum
 - exdisp/IShellWindows::_NewEnum
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
 - IShellWindows._NewEnum
---

# IShellWindows::_NewEnum


## -description

Retrieves an enumerator for the collection of Shell windows.

## -parameters

### -param ppunk [out, retval]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

When this method returns, contains an interface pointer to an object that implements the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/exdisp/nn-exdisp-ishellwindows">IShellWindows</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-item">IShellWindows::Item</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-get_count">IShellWindows::get_Count</a>