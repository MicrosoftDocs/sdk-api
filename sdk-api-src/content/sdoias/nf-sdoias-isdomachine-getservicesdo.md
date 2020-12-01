---
UID: NF:sdoias.ISdoMachine.GetServiceSDO
title: ISdoMachine::GetServiceSDO (sdoias.h)
description: The GetServiceSDO method retrieves a Server Data Object (SDO) for the specified service.
helpviewer_keywords: ["IAS","RemoteAccess","GetServiceSDO","GetServiceSDO method [Network Policy Server]","GetServiceSDO method [Network Policy Server]","ISdoMachine interface","GetServiceSDO method [Network Policy Server]","SdoMachine object","ISdoMachine interface [Network Policy Server]","GetServiceSDO method","ISdoMachine.GetServiceSDO","ISdoMachine::GetServiceSDO","SdoMachine object [Network Policy Server]","GetServiceSDO method","_sdo_isdomachine_getservicesdo","nps.SDO_isdomachine_getservicesdo","sdo.isdomachine_getservicesdo","sdoias/ISdoMachine::GetServiceSDO"]
old-location: nps\SDO_isdomachine_getservicesdo.htm
tech.root: Nps
ms.assetid: 265f034a-78be-4792-958e-80ad7a71d1a7
ms.date: 12/05/2018
ms.keywords: IAS, RemoteAccess, GetServiceSDO, GetServiceSDO method [Network Policy Server], GetServiceSDO method [Network Policy Server],ISdoMachine interface, GetServiceSDO method [Network Policy Server],SdoMachine object, ISdoMachine interface [Network Policy Server],GetServiceSDO method, ISdoMachine.GetServiceSDO, ISdoMachine::GetServiceSDO, SdoMachine object [Network Policy Server],GetServiceSDO method, _sdo_isdomachine_getservicesdo, nps.SDO_isdomachine_getservicesdo, sdo.isdomachine_getservicesdo, sdoias/ISdoMachine::GetServiceSDO
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
 - ISdoMachine::GetServiceSDO
 - sdoias/ISdoMachine::GetServiceSDO
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
 - ISdoMachine.GetServiceSDO
 - SdoMachine.GetServiceSDO
---

# ISdoMachine::GetServiceSDO


## -description

The <b>GetServiceSDO</b> method retrieves a 
    Server Data Object (SDO) for the specified service.

## -parameters

### -param eDataStore [in]

Specifies a value from the <a href="/windows/desktop/api/sdoias/ne-sdoias-iasdatastore">IASDATASTORE</a> enumeration 
      type.

### -param bstrServiceName [in]

Specifies a 
      <a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> that contains the service 
      name. This parameter is one of the following values.



#### "IAS"

Network Policy Server

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server starting with 
         Windows Server 2008.</div>
<div> </div>


#### "RemoteAccess"

Remote Access Server

### -param ppServiceSDO [out]

Pointer to a pointer that points to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface 
      pointer. Use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of this 
      <b>IUnknown</b> interface to obtain an 
      <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface for the 
      <a href="/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol">ISdoServiceControl</a> object.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -remarks

Before calling this method, use the 
    <a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach">ISdoMachine::Attach</a> method to attach to the SDO 
    computer.

None of the parameters for this method can be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/sdoias/nn-sdoias-isdomachine">ISdoMachine</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach">ISdoMachine::Attach</a>



<a href="/windows/desktop/Nps/sdo-retrieving-a-service-sdo">Retrieving a Service SDO</a>