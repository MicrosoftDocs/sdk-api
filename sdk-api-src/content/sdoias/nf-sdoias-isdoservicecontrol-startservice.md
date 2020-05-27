---
UID: NF:sdoias.ISdoServiceControl.StartService
title: ISdoServiceControl::StartService (sdoias.h)
description: The StartService method starts the service administered through SDO.
helpviewer_keywords: ["ISdoServiceControl interface [Network Policy Server]","StartService method","ISdoServiceControl.StartService","ISdoServiceControl::StartService","StartService","StartService method [Network Policy Server]","StartService method [Network Policy Server]","ISdoServiceControl interface","_sdo_isdoservicecontrol_startservice","nps.SDO_isdoservicecontrol_startservice","sdo.isdoservicecontrol_startservice","sdoias/ISdoServiceControl::StartService"]
old-location: nps\SDO_isdoservicecontrol_startservice.htm
tech.root: Nps
ms.assetid: f024a3b8-c527-4a43-99df-c5b146dae1b8
ms.date: 12/05/2018
ms.keywords: ISdoServiceControl interface [Network Policy Server],StartService method, ISdoServiceControl.StartService, ISdoServiceControl::StartService, StartService, StartService method [Network Policy Server], StartService method [Network Policy Server],ISdoServiceControl interface, _sdo_isdoservicecontrol_startservice, nps.SDO_isdoservicecontrol_startservice, sdo.isdoservicecontrol_startservice, sdoias/ISdoServiceControl::StartService
f1_keywords:
- sdoias/ISdoServiceControl.StartService
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo">ISdoMachineGetServiceSDO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol">ISdoServiceControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdoservicecontrol-getservicestatus">ISdoServiceControl::GetServiceStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdoservicecontrol-stopservice">ISdoServiceControl::StopService</a>
 

 

