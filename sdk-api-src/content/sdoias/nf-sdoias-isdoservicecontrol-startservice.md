---
UID: NF:sdoias.ISdoServiceControl.StartService
title: ISdoServiceControl::StartService
author: windows-sdk-content
description: The StartService method starts the service administered through SDO.
old-location: nps\SDO_isdoservicecontrol_startservice.htm
tech.root: Nps
ms.assetid: f024a3b8-c527-4a43-99df-c5b146dae1b8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISdoServiceControl interface [Network Policy Server],StartService method, ISdoServiceControl.StartService, ISdoServiceControl::StartService, StartService, StartService method [Network Policy Server], StartService method [Network Policy Server],ISdoServiceControl interface, _sdo_isdoservicecontrol_startservice, nps.SDO_isdoservicecontrol_startservice, sdo.isdoservicecontrol_startservice, sdoias/ISdoServiceControl::StartService
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISdoServiceControl.StartService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISdoServiceControl::StartService


## -description


The 
<b>StartService</b> method starts the service administered through SDO.


## -parameters






## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Calls to this method return almost immediately. NPS (IAS) takes several minutes to start up if its SDO configuration database contains a large number of objects.

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/265f034a-78be-4792-958e-80ad7a71d1a7">ISdoMachineGetServiceSDO</a>



<a href="https://msdn.microsoft.com/c901ac9a-524a-498d-8b72-9afb26cf2c58">ISdoServiceControl</a>



<a href="https://msdn.microsoft.com/6ef65e85-d77d-4f59-aaac-c0b5b337b564">ISdoServiceControl::GetServiceStatus</a>



<a href="https://msdn.microsoft.com/a90e4d12-589b-4d28-89e6-6c0ec6900b0a">ISdoServiceControl::StopService</a>
 

 

