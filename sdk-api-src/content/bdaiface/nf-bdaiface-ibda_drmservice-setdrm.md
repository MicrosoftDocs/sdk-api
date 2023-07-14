---
UID: NF:bdaiface.IBDA_DRMService.SetDRM
title: IBDA_DRMService::SetDRM (bdaiface.h)
description: Activates a digital rights management (DRM) system on the media transform device (MTD).
helpviewer_keywords: ["IBDA_DRMService interface [Microsoft TV Technologies]","SetDRM method","IBDA_DRMService.SetDRM","IBDA_DRMService::SetDRM","SetDRM","SetDRM method [Microsoft TV Technologies]","SetDRM method [Microsoft TV Technologies]","IBDA_DRMService interface","bdaiface/IBDA_DRMService::SetDRM","mstv.ibda_drmservice_setdrm"]
old-location: mstv\ibda_drmservice_setdrm.htm
tech.root: mstv
ms.assetid: 89da348f-c79c-4c77-8270-51a71b0a1a89
ms.date: 12/05/2018
ms.keywords: IBDA_DRMService interface [Microsoft TV Technologies],SetDRM method, IBDA_DRMService.SetDRM, IBDA_DRMService::SetDRM, SetDRM, SetDRM method [Microsoft TV Technologies], SetDRM method [Microsoft TV Technologies],IBDA_DRMService interface, bdaiface/IBDA_DRMService::SetDRM, mstv.ibda_drmservice_setdrm
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_DRMService::SetDRM
 - bdaiface/IBDA_DRMService::SetDRM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_DRMService.SetDRM
---

# IBDA_DRMService::SetDRM


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Activates a digital rights management (DRM) system on the media transform device (MTD).

## -parameters

### -param puuidNewDrm [in]

Pointer to a GUID that specifies the DRM system.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_drmservice">IBDA_DRMService</a>