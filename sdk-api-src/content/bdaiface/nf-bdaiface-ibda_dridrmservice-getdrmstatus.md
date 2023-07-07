---
UID: NF:bdaiface.IBDA_DRIDRMService.GetDRMStatus
title: IBDA_DRIDRMService::GetDRMStatus (bdaiface.h)
description: The GetDRMSTatus method returns the current status of the Digital Rights Management (DRM) system for a Media Transform Device (MTD) in a graph under the Protected Broadcast Device Architecture (PBDA).
helpviewer_keywords: ["GetDRMStatus","GetDRMStatus method [DirectShow]","GetDRMStatus method [DirectShow]","IBDA_DRIDRMService interface","IBDA_DRIDRMService interface [DirectShow]","GetDRMStatus method","IBDA_DRIDRMService.GetDRMStatus","IBDA_DRIDRMService::GetDRMStatus","bdaiface/IBDA_DRIDRMService::GetDRMStatus","mstv.ibda_dridrmservice_getdrmstatus"]
old-location: mstv\ibda_dridrmservice_getdrmstatus.htm
tech.root: mstv
ms.assetid: 145e4716-05e1-41b8-98f3-72e719ca8b9f
ms.date: 12/05/2018
ms.keywords: GetDRMStatus, GetDRMStatus method [DirectShow], GetDRMStatus method [DirectShow],IBDA_DRIDRMService interface, IBDA_DRIDRMService interface [DirectShow],GetDRMStatus method, IBDA_DRIDRMService.GetDRMStatus, IBDA_DRIDRMService::GetDRMStatus, bdaiface/IBDA_DRIDRMService::GetDRMStatus, mstv.ibda_dridrmservice_getdrmstatus
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
 - IBDA_DRIDRMService::GetDRMStatus
 - bdaiface/IBDA_DRIDRMService::GetDRMStatus
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
 - IBDA_DRIDRMService.GetDRMStatus
---

# IBDA_DRIDRMService::GetDRMStatus


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The GetDRMSTatus method returns the current status of the Digital Rights Management (DRM) system for a Media Transform Device (MTD) in a graph under the Protected Broadcast Device Architecture (PBDA).

## -parameters

### -param pbstrDrmUuidList [out]

Address of a variable that gets a comma-delimited string of UUID values that identify the DRM systems supported by the MTD. This method allocates the memory for the variable by calling <b>SysAllocString</b> and returns the associated pointer in this parameter. The caller is memory and is responsible for deallocating it by calling <b>SysFreeString</b>.

### -param DrmUuid [out]

Address of a variable that gets a GUID identifying the active DRM system for the MTD.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_dridrmservice">IBDA_DRIDRMService</a>