---
UID: NF:bdaiface.IBDA_DRIDRMService.GetDRMStatus
title: IBDA_DRIDRMService::GetDRMStatus
author: windows-sdk-content
description: The GetDRMSTatus method returns the current status of the Digital Rights Management (DRM) system for a Media Transform Device (MTD) in a graph under the Protected Broadcast Device Architecture (PBDA).
old-location: mstv\ibda_dridrmservice_getdrmstatus.htm
old-project: mstv
ms.assetid: 145e4716-05e1-41b8-98f3-72e719ca8b9f
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetDRMStatus, GetDRMStatus method [DirectShow], GetDRMStatus method [DirectShow],IBDA_DRIDRMService interface, IBDA_DRIDRMService interface [DirectShow],GetDRMStatus method, IBDA_DRIDRMService.GetDRMStatus, IBDA_DRIDRMService::GetDRMStatus, bdaiface/IBDA_DRIDRMService::GetDRMStatus, mstv.ibda_dridrmservice_getdrmstatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_DRIDRMService.GetDRMStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_DRIDRMService::GetDRMStatus


## -description



      The GetDRMSTatus method returns the current status of the Digital Rights Management (DRM) system for a Media Transform Device (MTD) in a graph under the Protected Broadcast Device Architecture (PBDA). 


## -parameters




### -param pbstrDrmUuidList [out]

Address of a variable that gets a comma-delimited string of UUID values that identify the DRM systems supported by the MTD. This method allocates the memory for the variable by calling <b>SysAllocString</b> and returns the associated pointer in this parameter. The caller is memory and is responsible for deallocating it by calling <b>SysFreeString</b>.
          


### -param DrmUuid [out]


            Address of a variable that gets a GUID identifying the active DRM system for the MTD.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9b04c960-a766-4322-bf18-e59176ee2ad1">IBDA_DRIDRMService</a>
 

 

