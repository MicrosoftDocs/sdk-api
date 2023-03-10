---
UID: NS:rtmv2._RTM_REGN_PROFILE
title: RTM_REGN_PROFILE (rtmv2.h)
description: The RTM_REGN_PROFILE structure contains information returned during the registration process. The information is used for later function calls (such as the maximum number of routes that can be returned by a call to RtmGetEnumRoutes).
helpviewer_keywords: ["*PRTM_REGN_PROFILE","PRTM_REGN_PROFILE","PRTM_REGN_PROFILE structure pointer [RAS]","RTM_REGN_PROFILE","RTM_REGN_PROFILE structure [RAS]","_rtmv2ref_rtm_regn_profile","rras.rtm_regn_profile","rtmv2/PRTM_REGN_PROFILE","rtmv2/RTM_REGN_PROFILE"]
old-location: rras\rtm_regn_profile.htm
tech.root: RRAS
ms.assetid: 26644a09-8d49-4c9f-a7cd-5edbf93e83d0
ms.date: 12/05/2018
ms.keywords: '*PRTM_REGN_PROFILE, PRTM_REGN_PROFILE, PRTM_REGN_PROFILE structure pointer [RAS], RTM_REGN_PROFILE, RTM_REGN_PROFILE structure [RAS], _rtmv2ref_rtm_regn_profile, rras.rtm_regn_profile, rtmv2/PRTM_REGN_PROFILE, rtmv2/RTM_REGN_PROFILE'
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RTM_REGN_PROFILE, *PRTM_REGN_PROFILE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RTM_REGN_PROFILE
 - rtmv2/_RTM_REGN_PROFILE
 - PRTM_REGN_PROFILE
 - rtmv2/PRTM_REGN_PROFILE
 - RTM_REGN_PROFILE
 - rtmv2/RTM_REGN_PROFILE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_REGN_PROFILE
---

# RTM_REGN_PROFILE structure


## -description

The 
<b>RTM_REGN_PROFILE</b> structure contains information returned during the registration process. The information is used for later function calls (such as the maximum number of routes that can be returned by a call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumroutes">RtmGetEnumRoutes</a>).

## -struct-fields

### -field MaxNextHopsInRoute

Specifies the maximum number of equal-cost next hops in a route.

### -field MaxHandlesInEnum

Specifies the maximum number of handles that can be returned in one call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumdests">RtmGetEnumDests</a>, 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetchangeddests">RtmGetChangedDests</a>, 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumroutes">RtmGetEnumRoutes</a>, or 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetlistenumroutes">RtmGetListEnumRoutes</a>. The number of handles that can be returned is limited (and configurable) to improve efficiency and performance of the routing table manager.

### -field ViewsSupported

Views supported by this address family.

### -field NumberOfViews

Number of views.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>