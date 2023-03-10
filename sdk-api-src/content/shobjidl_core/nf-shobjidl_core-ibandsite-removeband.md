---
UID: NF:shobjidl_core.IBandSite.RemoveBand
title: IBandSite::RemoveBand (shobjidl_core.h)
description: Removes a band from the band site.
helpviewer_keywords: ["IBandSite interface [Windows Shell]","RemoveBand method","IBandSite.RemoveBand","IBandSite::RemoveBand","RemoveBand","RemoveBand method [Windows Shell]","RemoveBand method [Windows Shell]","IBandSite interface","_win32_IBandSite_RemoveBand","shell.IBandSite_RemoveBand","shobjidl_core/IBandSite::RemoveBand"]
old-location: shell\IBandSite_RemoveBand.htm
tech.root: shell
ms.assetid: 5af20633-fab4-4fda-84c9-6bbdb9d588ec
ms.date: 12/05/2018
ms.keywords: IBandSite interface [Windows Shell],RemoveBand method, IBandSite.RemoveBand, IBandSite::RemoveBand, RemoveBand, RemoveBand method [Windows Shell], RemoveBand method [Windows Shell],IBandSite interface, _win32_IBandSite_RemoveBand, shell.IBandSite_RemoveBand, shobjidl_core/IBandSite::RemoveBand
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
 - IBandSite::RemoveBand
 - shobjidl_core/IBandSite::RemoveBand
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
 - IBandSite.RemoveBand
---

# IBandSite::RemoveBand


## -description

Removes a band from the band site.

## -parameters

### -param dwBandID [in]

Type: <b>DWORD</b>

The ID of the band to remove.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ibandsite">IBandSite</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a>