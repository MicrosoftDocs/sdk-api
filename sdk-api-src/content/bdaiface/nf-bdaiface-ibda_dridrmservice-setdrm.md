---
UID: NF:bdaiface.IBDA_DRIDRMService.SetDRM
title: IBDA_DRIDRMService::SetDRM (bdaiface.h)
description: Selects a Digital Rights Management (DRM) application for a Media Transform Device (MTD) in a Protected Broadcast Device Architecture (PBDA) graph.
helpviewer_keywords: ["IBDA_DRIDRMService interface [DirectShow]","SetDRM method","IBDA_DRIDRMService.SetDRM","IBDA_DRIDRMService::SetDRM","SetDRM","SetDRM method [DirectShow]","SetDRM method [DirectShow]","IBDA_DRIDRMService interface","bdaiface/IBDA_DRIDRMService::SetDRM","mstv.ibda_dridrmservice_setdrm"]
old-location: mstv\ibda_dridrmservice_setdrm.htm
tech.root: mstv
ms.assetid: 95e59f33-0ff4-4618-b1e8-c43fe60b9434
ms.date: 12/05/2018
ms.keywords: IBDA_DRIDRMService interface [DirectShow],SetDRM method, IBDA_DRIDRMService.SetDRM, IBDA_DRIDRMService::SetDRM, SetDRM, SetDRM method [DirectShow], SetDRM method [DirectShow],IBDA_DRIDRMService interface, bdaiface/IBDA_DRIDRMService::SetDRM, mstv.ibda_dridrmservice_setdrm
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IBDA_DRIDRMService::SetDRM
 - bdaiface/IBDA_DRIDRMService::SetDRM
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
 - IBDA_DRIDRMService.SetDRM
---

# IBDA_DRIDRMService::SetDRM


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Selects a Digital Rights Management (DRM) application for a Media Transform Device (MTD) in a Protected Broadcast Device Architecture (PBDA) graph. The MTD sets the DRMPairingStatus value to "Red", which indicates an unpaired state, and switches to the designated DRM application within five seconds.

## -parameters

### -param bstrNewDrm [in]

Address of the GUID that identifies the new DRM application.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_dridrmservice">IBDA_DRIDRMService</a>