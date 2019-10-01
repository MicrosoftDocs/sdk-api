---
UID: NF:sdoias.ISdoServiceControl.ResetService
title: ISdoServiceControl::ResetService (sdoias.h)
author: windows-sdk-content
description: The ResetService method resets the service administered by the SDO API. Resetting the service causes the service to refresh its data.
old-location: nps\SDO_isdoservicecontrol_resetservice.htm
tech.root: Nps
ms.assetid: c93675ad-b7c2-42b9-9ab8-7fb4cbb7a07c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISdoServiceControl interface [Network Policy Server],ResetService method, ISdoServiceControl.ResetService, ISdoServiceControl::ResetService, ResetService, ResetService method [Network Policy Server], ResetService method [Network Policy Server],ISdoServiceControl interface, _sdo_isdoservicecontrol_resetservice, nps.SDO_isdoservicecontrol_resetservice, sdo.isdoservicecontrol_resetservice, sdoias/ISdoServiceControl::ResetService
ms.topic: method
f1_keywords: 
 - "sdoias/ISdoServiceControl.ResetService"
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Iassdo.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoServiceControl.ResetService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISdoServiceControl::ResetService


## -description


The <b>ResetService</b> method resets the 
  service administered by the SDO API. Resetting the service causes the service to refresh its data.


## -parameters






## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



The data refresh begins 5 seconds after the last call to 
  <b>ISdoServiceControl::ResetService</b>. The 
  amount of time it takes for the refresh to complete depends on the number of objects in the SDO configuration 
  database.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo">ISdoMachineGetServiceSDO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol">ISdoServiceControl</a>
 

 

