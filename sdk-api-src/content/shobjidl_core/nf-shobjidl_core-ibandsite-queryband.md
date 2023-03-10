---
UID: NF:shobjidl_core.IBandSite.QueryBand
title: IBandSite::QueryBand (shobjidl_core.h)
description: Gets information about a band in a band site.
helpviewer_keywords: ["IBandSite interface [Windows Shell]","QueryBand method","IBandSite.QueryBand","IBandSite::QueryBand","QueryBand","QueryBand method [Windows Shell]","QueryBand method [Windows Shell]","IBandSite interface","_win32_IBandSite_QueryBand","shell.IBandSite_QueryBand","shobjidl_core/IBandSite::QueryBand"]
old-location: shell\IBandSite_QueryBand.htm
tech.root: shell
ms.assetid: 0618ad7d-4e8f-4fbf-ab64-2b1c0d42158c
ms.date: 12/05/2018
ms.keywords: IBandSite interface [Windows Shell],QueryBand method, IBandSite.QueryBand, IBandSite::QueryBand, QueryBand, QueryBand method [Windows Shell], QueryBand method [Windows Shell],IBandSite interface, _win32_IBandSite_QueryBand, shell.IBandSite_QueryBand, shobjidl_core/IBandSite::QueryBand
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
 - IBandSite::QueryBand
 - shobjidl_core/IBandSite::QueryBand
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
 - IBandSite.QueryBand
---

# IBandSite::QueryBand


## -description

Gets information about a band in a band site.

## -parameters

### -param dwBandID [in]

Type: <b>DWORD</b>

The ID of the band object to query.

### -param ppstb [out, optional]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a>**</b>

Address of an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a> interface pointer that, when this method returns successfully, points to the <b>IDeskBand</b> object that represents the band. This value can be <b>NULL</b>.

### -param pdwState [out, optional]

Type: <b>DWORD*</b>

Pointer to a <b>DWORD</b> value that, when this method returns successfully, receives the state of the band object. This state is a combination of BSSF_VISIBLE, BSSF_NOTITLE, and BSSF_UNDELETEABLE. See <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo">BANDSITEINFO</a> for more information on those flags. This value can be <b>NULL</b> if the state information is not needed.

### -param pszName [out]

Type: <b>LPWSTR</b>

Pointer to a buffer of <i>cchName</i> Unicode characters that, when this method returns successfully, receives the name of the band object.

### -param cchName [in]

Type: <b>int</b>

The size of the <i>pszName</i> buffer, in characters.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.