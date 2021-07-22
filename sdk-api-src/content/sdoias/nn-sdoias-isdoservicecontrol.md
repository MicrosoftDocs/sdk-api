---
UID: NN:sdoias.ISdoServiceControl
title: ISdoServiceControl (sdoias.h)
description: Use the ISdoServiceControl interface to control the service being administered on the SDO computer.
helpviewer_keywords: ["ISdoServiceControl","ISdoServiceControl interface [Network Policy Server]","ISdoServiceControl interface [Network Policy Server]","described","_sdo_isdoservicecontrol","nps.SDO_isdoservicecontrol","sdo.isdoservicecontrol","sdoias/ISdoServiceControl"]
old-location: nps\SDO_isdoservicecontrol.htm
tech.root: Nps
ms.assetid: c901ac9a-524a-498d-8b72-9afb26cf2c58
ms.date: 12/05/2018
ms.keywords: ISdoServiceControl, ISdoServiceControl interface [Network Policy Server], ISdoServiceControl interface [Network Policy Server],described, _sdo_isdoservicecontrol, nps.SDO_isdoservicecontrol, sdo.isdoservicecontrol, sdoias/ISdoServiceControl
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
 - ISdoServiceControl
 - sdoias/ISdoServiceControl
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
 - ISdoServiceControl
---

# ISdoServiceControl interface


## -description

Use the 
<b>ISdoServiceControl</b> interface to control the service being administered on the SDO computer.

## -inheritance

The <b>ISdoServiceControl</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISdoServiceControl</b> also has these types of members:

## -remarks

Use the 
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo">ISdoMachine::GetServiceSDO</a> method to retrieve a pointer to an 
<b>ISdoServiceControl</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/Nps/sdo-server-data-objects-interfaces">Server Data Objects Interfaces</a>



<a href="/windows/desktop/Nps/sdo-server-data-objects-reference">Server Data Objects Reference</a>
