---
UID: NF:shobjidl_core.IBandSite.AddBand
title: IBandSite::AddBand (shobjidl_core.h)
description: Adds a band to a band site object.
helpviewer_keywords: ["AddBand","AddBand method [Windows Shell]","AddBand method [Windows Shell]","IBandSite interface","IBandSite interface [Windows Shell]","AddBand method","IBandSite.AddBand","IBandSite::AddBand","_win32_IBandSite_AddBand","shell.IBandSite_AddBand","shobjidl_core/IBandSite::AddBand"]
old-location: shell\IBandSite_AddBand.htm
tech.root: shell
ms.assetid: a954aaf2-f862-4aea-8643-a5b453a8d8ee
ms.date: 12/05/2018
ms.keywords: AddBand, AddBand method [Windows Shell], AddBand method [Windows Shell],IBandSite interface, IBandSite interface [Windows Shell],AddBand method, IBandSite.AddBand, IBandSite::AddBand, _win32_IBandSite_AddBand, shell.IBandSite_AddBand, shobjidl_core/IBandSite::AddBand
req.header: shobjidl_core.h
req.include-header: Shldisp.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBandSite::AddBand
 - shobjidl_core/IBandSite::AddBand
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
 - IBandSite.AddBand
---

# IBandSite::AddBand


## -description

Adds a band to a band site object.

## -parameters

### -param punk [in]

Type: <b>IUnknown*</b>

The interface of a band site object.

## -returns

Type: <b>HRESULT</b>

Returns the band ID in ShortFromResult(hresult).

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ibandsite">IBandSite</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a>