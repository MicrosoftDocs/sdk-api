---
UID: NF:shobjidl_core.IBandSite.GetBandObject
title: IBandSite::GetBandObject (shobjidl_core.h)
description: Gets a specified band object from a band site.
helpviewer_keywords: ["GetBandObject","GetBandObject method [Windows Shell]","GetBandObject method [Windows Shell]","IBandSite interface","IBandSite interface [Windows Shell]","GetBandObject method","IBandSite.GetBandObject","IBandSite::GetBandObject","_win32_IBandSite_GetBandObject","shell.IBandSite_GetBandObject","shobjidl_core/IBandSite::GetBandObject"]
old-location: shell\IBandSite_GetBandObject.htm
tech.root: shell
ms.assetid: e6eba36d-5fc8-4b79-8129-1e07c5cc5b5f
ms.date: 12/05/2018
ms.keywords: GetBandObject, GetBandObject method [Windows Shell], GetBandObject method [Windows Shell],IBandSite interface, IBandSite interface [Windows Shell],GetBandObject method, IBandSite.GetBandObject, IBandSite::GetBandObject, _win32_IBandSite_GetBandObject, shell.IBandSite_GetBandObject, shobjidl_core/IBandSite::GetBandObject
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
 - IBandSite::GetBandObject
 - shobjidl_core/IBandSite::GetBandObject
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
 - IBandSite.GetBandObject
---

# IBandSite::GetBandObject


## -description

Gets a specified band object from a band site.

## -parameters

### -param dwBandID [in]

Type: <b>DWORD</b>

The ID of the band object to get.

### -param riid [in]

Type: <b>REFIID</b>

The IID of the object to obtain.

### -param ppv [out]

Type: <b>VOID**</b>

The address of a pointer variable that receives a pointer
				to the object requested.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ibandsite">IBandSite</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a>