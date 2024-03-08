---
UID: NF:bdaiface.IBDA_DRMService.GetDRMStatus
title: IBDA_DRMService::GetDRMStatus (bdaiface.h)
description: Gets the current digital rights management (DRM) status.
helpviewer_keywords: ["GetDRMStatus","GetDRMStatus method [Microsoft TV Technologies]","GetDRMStatus method [Microsoft TV Technologies]","IBDA_DRMService interface","IBDA_DRMService interface [Microsoft TV Technologies]","GetDRMStatus method","IBDA_DRMService.GetDRMStatus","IBDA_DRMService::GetDRMStatus","bdaiface/IBDA_DRMService::GetDRMStatus","mstv.ibda_drmservice_getdrmstatus"]
old-location: mstv\ibda_drmservice_getdrmstatus.htm
tech.root: mstv
ms.assetid: 474ea991-6fb4-4eb4-9146-c76914765dc1
ms.date: 12/05/2018
ms.keywords: GetDRMStatus, GetDRMStatus method [Microsoft TV Technologies], GetDRMStatus method [Microsoft TV Technologies],IBDA_DRMService interface, IBDA_DRMService interface [Microsoft TV Technologies],GetDRMStatus method, IBDA_DRMService.GetDRMStatus, IBDA_DRMService::GetDRMStatus, bdaiface/IBDA_DRMService::GetDRMStatus, mstv.ibda_drmservice_getdrmstatus
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
 - IBDA_DRMService::GetDRMStatus
 - bdaiface/IBDA_DRMService::GetDRMStatus
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
 - IBDA_DRMService.GetDRMStatus
---

# IBDA_DRMService::GetDRMStatus


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the current digital rights management (DRM) status.

## -parameters

### -param pbstrDrmUuidList [out]

Receives a comma-separated list of GUIDs that identify the DRM systems supported by the media transform device (MTD). Each GUID is represented in following format: "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx". The caller must release the string by calling <b>SysFreeString</b>.

### -param DrmUuid [out]

Receives a GUID that identifies which DRM system is currently active.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_drmservice">IBDA_DRMService</a>