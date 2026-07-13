---
UID: NF:gpmgmt.IGPMResult.OverallStatus
title: IGPMResult::OverallStatus (gpmgmt.h)
description: Returns the overall status of a GPMC operation, such as a copy, restore, backup, or import. If no error occurred during the operation, the method returns a success code; otherwise the method returns a failure code.
helpviewer_keywords: ["GPMResult class [GPMC]","OverallStatus method","IGPMResult interface [GPMC]","OverallStatus method","IGPMResult.OverallStatus","IGPMResult::OverallStatus","OverallStatus","OverallStatus method [GPMC]","OverallStatus method [GPMC]","GPMResult class","OverallStatus method [GPMC]","IGPMResult interface","_win32_igpmresult_overallstatus","gpmc.igpmresult_overallstatus","gpmgmt/IGPMResult::OverallStatus"]
old-location: gpmc\igpmresult_overallstatus.htm
tech.root: gpmc
ms.assetid: 814c59b7-47bc-4757-997e-95ca578f544a
ms.date: 12/05/2018
ms.keywords: GPMResult class [GPMC],OverallStatus method, IGPMResult interface [GPMC],OverallStatus method, IGPMResult.OverallStatus, IGPMResult::OverallStatus, OverallStatus, OverallStatus method [GPMC], OverallStatus method [GPMC],GPMResult class, OverallStatus method [GPMC],IGPMResult interface, _win32_igpmresult_overallstatus, gpmc.igpmresult_overallstatus, gpmgmt/IGPMResult::OverallStatus
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMResult::OverallStatus
 - gpmgmt/IGPMResult::OverallStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMResult.OverallStatus
 - GPMResult.OverallStatus
---

# IGPMResult::OverallStatus


## -description

Returns the overall status of a GPMC operation, such as a copy, restore, backup, or import. If no error occurred during the operation, the method returns a success code; otherwise the method returns a failure code.
<div class="alert"><b>Note</b>  You must check the code returned by this method as well as the one returned by the GPMC operation to determine whether or not the operation succeeded.</div><div> </div>



## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a>
