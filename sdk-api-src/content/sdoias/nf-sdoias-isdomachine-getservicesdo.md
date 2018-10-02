---
UID: NF:sdoias.ISdoMachine.GetServiceSDO
title: ISdoMachine::GetServiceSDO
author: windows-sdk-content
description: The GetServiceSDO method retrieves a Server Data Object (SDO) for the specified service.
old-location: nps\SDO_isdomachine_getservicesdo.htm
tech.root: Nps
ms.assetid: 265f034a-78be-4792-958e-80ad7a71d1a7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ""IAS", "RemoteAccess", GetServiceSDO, GetServiceSDO method [Network Policy Server], GetServiceSDO method [Network Policy Server],ISdoMachine interface, GetServiceSDO method [Network Policy Server],SdoMachine object, ISdoMachine interface [Network Policy Server],GetServiceSDO method, ISdoMachine.GetServiceSDO, ISdoMachine::GetServiceSDO, SdoMachine object [Network Policy Server],GetServiceSDO method, _sdo_isdomachine_getservicesdo, nps.SDO_isdomachine_getservicesdo, sdo.isdomachine_getservicesdo, sdoias/ISdoMachine::GetServiceSDO"
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
 - ISdoMachine.GetServiceSDO
 - SdoMachine.GetServiceSDO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISdoMachine::GetServiceSDO


## -description


The <b>GetServiceSDO</b> method retrieves a 
    Server Data Object (SDO) for the specified service.


## -parameters




### -param eDataStore [in]

Specifies a value from the <a href="https://msdn.microsoft.com/1eec69f9-b82e-48e5-a471-0a0626d91957">IASDATASTORE</a> enumeration 
      type.


### -param bstrServiceName [in]

Specifies a 
      <a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> that contains the service 
      name. This parameter is one of the following values.



#### "IAS"

Network Policy Server

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server starting with 
         Windows Server 2008.</div>
<div> </div>


#### "RemoteAccess"

Remote Access Server


### -param ppServiceSDO [out]

Pointer to a pointer that points to an <a href="_com_iunknown">IUnknown</a> interface 
      pointer. Use the <a href="_com_iunknown_queryinterface">QueryInterface</a> method of this 
      <b>IUnknown</b> interface to obtain an 
      <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface for the 
      <a href="https://msdn.microsoft.com/c901ac9a-524a-498d-8b72-9afb26cf2c58">ISdoServiceControl</a> object.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Before calling this method, use the 
    <a href="https://msdn.microsoft.com/444ba670-8224-40bc-b0e4-585c682deafd">ISdoMachine::Attach</a> method to attach to the SDO 
    computer.

None of the parameters for this method can be <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/11372116-56eb-4d8e-8f28-4402835ee903">ISdoMachine</a>



<a href="https://msdn.microsoft.com/444ba670-8224-40bc-b0e4-585c682deafd">ISdoMachine::Attach</a>



<a href="https://msdn.microsoft.com/bac95c42-8f7e-4011-960c-8f18b4b7c088">Retrieving a Service SDO</a>
 

 

