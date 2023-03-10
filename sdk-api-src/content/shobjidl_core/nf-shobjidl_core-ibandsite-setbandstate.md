---
UID: NF:shobjidl_core.IBandSite.SetBandState
title: IBandSite::SetBandState (shobjidl_core.h)
description: Set the state of a band in the band site.
helpviewer_keywords: ["IBandSite interface [Windows Shell]","SetBandState method","IBandSite.SetBandState","IBandSite::SetBandState","SetBandState","SetBandState method [Windows Shell]","SetBandState method [Windows Shell]","IBandSite interface","_win32_IBandSite_SetBandState","shell.IBandSite_SetBandState","shobjidl_core/IBandSite::SetBandState"]
old-location: shell\IBandSite_SetBandState.htm
tech.root: shell
ms.assetid: d327f0fe-7d61-4edd-aff3-f4507763d751
ms.date: 12/05/2018
ms.keywords: IBandSite interface [Windows Shell],SetBandState method, IBandSite.SetBandState, IBandSite::SetBandState, SetBandState, SetBandState method [Windows Shell], SetBandState method [Windows Shell],IBandSite interface, _win32_IBandSite_SetBandState, shell.IBandSite_SetBandState, shobjidl_core/IBandSite::SetBandState
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
 - IBandSite::SetBandState
 - shobjidl_core/IBandSite::SetBandState
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
 - IBandSite.SetBandState
---

# IBandSite::SetBandState


## -description

Set the state of a band in the band site.

## -parameters

### -param dwBandID [in]

Type: <b>DWORD</b>

The ID of the band to set.  If this parameter is -1, then
				set the state of all bands in the band site.

### -param dwMask [in]

Type: <b>DWORD</b>

The mask of the states to set.

### -param dwState [in]

Type: <b>DWORD</b>

The state values to be set. These are combinations of
				BSSF_* flags. For more information, see <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo">BANDSITEINFO</a>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo">BANDSITEINFO</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ibandsite">IBandSite</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a>