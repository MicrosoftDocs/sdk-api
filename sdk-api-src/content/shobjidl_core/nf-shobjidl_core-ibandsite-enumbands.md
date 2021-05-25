---
UID: NF:shobjidl_core.IBandSite.EnumBands
title: IBandSite::EnumBands (shobjidl_core.h)
description: Enumerates the bands in a band site.
helpviewer_keywords: ["EnumBands","EnumBands method [Windows Shell]","EnumBands method [Windows Shell]","IBandSite interface","IBandSite interface [Windows Shell]","EnumBands method","IBandSite.EnumBands","IBandSite::EnumBands","_win32_IBandSite_EnumBands","shell.IBandSite_EnumBands","shobjidl_core/IBandSite::EnumBands"]
old-location: shell\IBandSite_EnumBands.htm
tech.root: shell
ms.assetid: d92ead78-9d58-48fe-ad93-33b2dbcbda68
ms.date: 12/05/2018
ms.keywords: EnumBands, EnumBands method [Windows Shell], EnumBands method [Windows Shell],IBandSite interface, IBandSite interface [Windows Shell],EnumBands method, IBandSite.EnumBands, IBandSite::EnumBands, _win32_IBandSite_EnumBands, shell.IBandSite_EnumBands, shobjidl_core/IBandSite::EnumBands
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
 - IBandSite::EnumBands
 - shobjidl_core/IBandSite::EnumBands
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
 - IBandSite.EnumBands
---

# IBandSite::EnumBands


## -description

Enumerates the bands in a band site.

## -parameters

### -param uBand [in]

Type: <b>UINT</b>

Call the method with this parameter starting at 0 to
				begin enumerating.  If this parameter is -1, the
       <i>pdwBandID</i> parameter is ignored and this method returns the count of the
				bands in the band site.

### -param pdwBandID [out]

Type: <b>DWORD*</b>

The address of a band ID variable that receives the band ID.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code for errors.
				If the first parameter is -1, the count of the bands in the band site
				is returned.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ibandsite">IBandSite</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a>