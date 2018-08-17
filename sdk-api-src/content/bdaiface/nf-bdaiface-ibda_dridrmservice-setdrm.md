---
UID: NF:bdaiface.IBDA_DRIDRMService.SetDRM
title: IBDA_DRIDRMService::SetDRM
author: windows-sdk-content
description: Selects a Digital Rights Management (DRM) application for a Media Transform Device (MTD) in a Protected Broadcast Device Architecture (PBDA) graph.
old-location: mstv\ibda_dridrmservice_setdrm.htm
old-project: mstv
ms.assetid: 95e59f33-0ff4-4618-b1e8-c43fe60b9434
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_DRIDRMService interface [DirectShow],SetDRM method, IBDA_DRIDRMService.SetDRM, IBDA_DRIDRMService::SetDRM, SetDRM, SetDRM method [DirectShow], SetDRM method [DirectShow],IBDA_DRIDRMService interface, bdaiface/IBDA_DRIDRMService::SetDRM, mstv.ibda_dridrmservice_setdrm
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_DRIDRMService.SetDRM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_DRIDRMService::SetDRM


## -description


Selects a Digital Rights Management (DRM) application for a Media Transform Device (MTD) in a Protected Broadcast Device Architecture (PBDA) graph. The MTD sets the DRMPairingStatus value to "Red", which indicates an unpaired state, and switches to the designated DRM application within five seconds.


## -parameters




### -param bstrNewDrm






#### - puuidNewDrm [in]

Address of the GUID that identifies the new DRM application.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd797840(v=VS.85).aspx">IBDA_DRIDRMService</a>
 

 

