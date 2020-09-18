---
UID: NF:shlwapi.IUnknown_SetSite
title: IUnknown_SetSite function (shlwapi.h)
description: Sets the specified object's site by calling its IObjectWithSite::SetSite method.
helpviewer_keywords: ["IUnknown_SetSite","IUnknown_SetSite function [Windows Shell]","_win32_IUnknown_SetSite","shell.IUnknown_SetSite","shlwapi/IUnknown_SetSite"]
old-location: shell\IUnknown_SetSite.htm
tech.root: shell
ms.assetid: 66175435-f85b-4e26-b148-f4edb74cb41d
ms.date: 12/05/2018
ms.keywords: IUnknown_SetSite, IUnknown_SetSite function [Windows Shell], _win32_IUnknown_SetSite, shell.IUnknown_SetSite, shlwapi/IUnknown_SetSite
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
 - IUnknown_SetSite
 - shlwapi/IUnknown_SetSite
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
 - IUnknown_SetSite
---

# IUnknown_SetSite function


## -description

Sets the specified object's site by calling its <a href="/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-setsite">IObjectWithSite::SetSite</a> method.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the IUnknown interface of the object whose site is to be changed.

### -param punkSite [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the IUnknown interface of the new site.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the site was successfully set, or a COM error code otherwise.

## -remarks

This function calls the specified object's IUnknown::QueryInterface method to obtain a pointer to the object's <a href="/windows/desktop/api/ocidl/nn-ocidl-iobjectwithsite">IObjectWithSite</a> interface.  If successful, the function calls <a href="/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-setsite">IObjectWithSite::SetSite</a> to set or change the site.