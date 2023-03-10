---
UID: NF:shlwapi.IUnknown_GetSite
title: IUnknown_GetSite function (shlwapi.h)
description: Calls the specified object's IObjectWithSite::GetSite method.
helpviewer_keywords: ["IUnknown_GetSite","IUnknown_GetSite function [Windows Shell]","_win32_IUnknown_GetSite","shell.IUnknown_GetSite","shlwapi/IUnknown_GetSite"]
old-location: shell\IUnknown_GetSite.htm
tech.root: shell
ms.assetid: 95e83078-ab74-40d6-8e31-653e578770f2
ms.date: 12/05/2018
ms.keywords: IUnknown_GetSite, IUnknown_GetSite function [Windows Shell], _win32_IUnknown_GetSite, shell.IUnknown_GetSite, shlwapi/IUnknown_GetSite
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
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
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUnknown_GetSite
 - shlwapi/IUnknown_GetSite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-comhelpers-l1-1-0.dll
api_name:
 - IUnknown_GetSite
---

# IUnknown_GetSite function


## -description

Calls the specified object's <a href="/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-getsite">IObjectWithSite::GetSite</a> method.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the COM object whose <a href="/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-getsite">IObjectWithSite::GetSite</a> method is to be called.

### -param riid [in]

Type: <b>REFIID</b>

The IID of the interface pointer that should be returned in <i>ppvSite</i>.

### -param ppv [out]

Type: <b>VOID**</b>

The address of the pointer to receive the requested interface pointer. If the function call is successful, <i>ppvSite</i> will contain the requested interface pointer. If no site is available or the requested interface is not supported, <i>ppvSite</i> is set to <b>NULL</b> and the function returns a COM error code.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the site was successfully retrieved or a COM error code otherwise.

## -remarks

This function calls the specified object's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method to obtain the <a href="/windows/desktop/api/ocidl/nn-ocidl-iobjectwithsite">IObjectWithSite</a> interface.  If successful, the function calls the interface's <a href="/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-getsite">IObjectWithSite::GetSite</a> method to obtain the site.