---
UID: NF:shobjidl_core.IBandSite.GetBandSiteInfo
title: IBandSite::GetBandSiteInfo (shobjidl_core.h)
description: Gets information about a band in the band site.
helpviewer_keywords: ["GetBandSiteInfo","GetBandSiteInfo method [Windows Shell]","GetBandSiteInfo method [Windows Shell]","IBandSite interface","IBandSite interface [Windows Shell]","GetBandSiteInfo method","IBandSite.GetBandSiteInfo","IBandSite::GetBandSiteInfo","_win32_IBandSite_GetBandSiteInfo","shell.IBandSite_GetBandSiteInfo","shobjidl_core/IBandSite::GetBandSiteInfo"]
old-location: shell\IBandSite_GetBandSiteInfo.htm
tech.root: shell
ms.assetid: 5831de51-f785-430e-b7e6-f1f40a83357b
ms.date: 12/05/2018
ms.keywords: GetBandSiteInfo, GetBandSiteInfo method [Windows Shell], GetBandSiteInfo method [Windows Shell],IBandSite interface, IBandSite interface [Windows Shell],GetBandSiteInfo method, IBandSite.GetBandSiteInfo, IBandSite::GetBandSiteInfo, _win32_IBandSite_GetBandSiteInfo, shell.IBandSite_GetBandSiteInfo, shobjidl_core/IBandSite::GetBandSiteInfo
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
 - IBandSite::GetBandSiteInfo
 - shobjidl_core/IBandSite::GetBandSiteInfo
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
 - IBandSite.GetBandSiteInfo
---

# IBandSite::GetBandSiteInfo


## -description

Gets information about a band in the band site.

## -parameters

### -param pbsinfo [in, out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo">BANDSITEINFO</a>*</b>

The address of a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo">BANDSITEINFO</a> structure that contains
				the band site information for the object. The
				<b>dwMask</b> member of this structure
				specifies what information is being requested.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo">BANDSITEINFO</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ibandsite">IBandSite</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a>