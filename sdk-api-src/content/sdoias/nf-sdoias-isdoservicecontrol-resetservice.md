---
UID: NF:sdoias.ISdoServiceControl.ResetService
title: ISdoServiceControl::ResetService
author: windows-sdk-content
description: The ResetService method resets the service administered by the SDO API. Resetting the service causes the service to refresh its data.
old-location: nps\SDO_isdoservicecontrol_resetservice.htm
old-project: Nps
ms.assetid: c93675ad-b7c2-42b9-9ab8-7fb4cbb7a07c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ISdoServiceControl interface [Network Policy Server],ResetService method, ISdoServiceControl.ResetService, ISdoServiceControl::ResetService, ResetService, ResetService method [Network Policy Server], ResetService method [Network Policy Server],ISdoServiceControl interface, _sdo_isdoservicecontrol_resetservice, nps.SDO_isdoservicecontrol_resetservice, sdo.isdoservicecontrol_resetservice, sdoias/ISdoServiceControl::ResetService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VENDORPROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoServiceControl.ResetService
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: ADAM
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




<a href="https://msdn.microsoft.com/265f034a-78be-4792-958e-80ad7a71d1a7">ISdoMachineGetServiceSDO</a>



<a href="https://msdn.microsoft.com/c901ac9a-524a-498d-8b72-9afb26cf2c58">ISdoServiceControl</a>
 

 

