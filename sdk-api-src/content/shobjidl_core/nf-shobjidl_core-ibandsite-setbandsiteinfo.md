---
UID: NF:shobjidl_core.IBandSite.SetBandSiteInfo
title: IBandSite::SetBandSiteInfo (shobjidl_core.h)
description: Sets information about the band site.
helpviewer_keywords: ["IBandSite interface [Windows Shell]","SetBandSiteInfo method","IBandSite.SetBandSiteInfo","IBandSite::SetBandSiteInfo","SetBandSiteInfo","SetBandSiteInfo method [Windows Shell]","SetBandSiteInfo method [Windows Shell]","IBandSite interface","_win32_IBandSite_SetBandSiteInfo","shell.IBandSite_SetBandSiteInfo","shobjidl_core/IBandSite::SetBandSiteInfo"]
old-location: shell\IBandSite_SetBandSiteInfo.htm
tech.root: shell
ms.assetid: 2658a49d-d60f-483b-bbe1-e1390e9dc35e
ms.date: 12/05/2018
ms.keywords: IBandSite interface [Windows Shell],SetBandSiteInfo method, IBandSite.SetBandSiteInfo, IBandSite::SetBandSiteInfo, SetBandSiteInfo, SetBandSiteInfo method [Windows Shell], SetBandSiteInfo method [Windows Shell],IBandSite interface, _win32_IBandSite_SetBandSiteInfo, shell.IBandSite_SetBandSiteInfo, shobjidl_core/IBandSite::SetBandSiteInfo
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
 - IBandSite::SetBandSiteInfo
 - shobjidl_core/IBandSite::SetBandSiteInfo
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
 - IBandSite.SetBandSiteInfo
---

# IBandSite::SetBandSiteInfo


## -description

Sets information about the band site.

## -parameters

### -param pbsinfo [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo">BANDSITEINFO</a>*</b>

The address of a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo">BANDSITEINFO</a> structure that receives
				the band site information for the object. The
				<b>dwMask</b> member of this structure
				specifies what information is being set.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ibandsite">IBandSite</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ideskband">IDeskBand</a>