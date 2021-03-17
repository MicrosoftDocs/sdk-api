---
UID: NF:sdoias.ISdoServiceControl.GetServiceStatus
title: ISdoServiceControl::GetServiceStatus (sdoias.h)
description: The GetServiceStatus method retrieves the status of the service being administered through SDO.
helpviewer_keywords: ["GetServiceStatus","GetServiceStatus method [Network Policy Server]","GetServiceStatus method [Network Policy Server]","ISdoServiceControl interface","ISdoServiceControl interface [Network Policy Server]","GetServiceStatus method","ISdoServiceControl.GetServiceStatus","ISdoServiceControl::GetServiceStatus","SERVICE_RUNNING","SERVICE_START_PENDING","SERVICE_STOPPED","SERVICE_STOP_PENDING","_sdo_isdoservicecontrol_getservicestatus","nps.SDO_isdoservicecontrol_getservicestatus","sdo.isdoservicecontrol_getservicestatus","sdoias/ISdoServiceControl::GetServiceStatus"]
old-location: nps\SDO_isdoservicecontrol_getservicestatus.htm
tech.root: Nps
ms.assetid: 6ef65e85-d77d-4f59-aaac-c0b5b337b564
ms.date: 12/05/2018
ms.keywords: GetServiceStatus, GetServiceStatus method [Network Policy Server], GetServiceStatus method [Network Policy Server],ISdoServiceControl interface, ISdoServiceControl interface [Network Policy Server],GetServiceStatus method, ISdoServiceControl.GetServiceStatus, ISdoServiceControl::GetServiceStatus, SERVICE_RUNNING, SERVICE_START_PENDING, SERVICE_STOPPED, SERVICE_STOP_PENDING, _sdo_isdoservicecontrol_getservicestatus, nps.SDO_isdoservicecontrol_getservicestatus, sdo.isdoservicecontrol_getservicestatus, sdoias/ISdoServiceControl::GetServiceStatus
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISdoServiceControl::GetServiceStatus
 - sdoias/ISdoServiceControl::GetServiceStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoServiceControl.GetServiceStatus
---

# ISdoServiceControl::GetServiceStatus


## -description

The <b>GetServiceStatus</b> method 
    retrieves the status of the service being administered through SDO.

## -parameters

### -param status [out]

Pointer to a <b>LONG</b> variable that contains the status of the service. The status 
      is one of the following values.



#### SERVICE_STOPPED

The service is stopped.



#### SERVICE_START_PENDING

The service is starting.



#### SERVICE_STOP_PENDING

The service is shutting down.



#### SERVICE_RUNNING

The service is up and running.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -see-also

<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo">ISdoMachine::GetServiceSDO</a>



<a href="/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol">ISdoServiceControl</a>