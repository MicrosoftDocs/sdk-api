---
UID: NF:sdoias.ISdoMachine.GetDomainType
title: ISdoMachine::GetDomainType
author: windows-driver-content
description: The GetDomainType retrieves the type of domain in which the SDO computer resides.
old-location: nps\SDO_isdomachine_getdomaintype.htm
old-project: Nps
ms.assetid: 9c22ec67-4a12-4487-bac5-8f0e666b8029
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: GetDomainType, GetDomainType method [Network Policy Server], GetDomainType method [Network Policy Server],ISdoMachine interface, GetDomainType method [Network Policy Server],SdoMachine object, ISdoMachine interface [Network Policy Server],GetDomainType method, ISdoMachine.GetDomainType, ISdoMachine::GetDomainType, SdoMachine object [Network Policy Server],GetDomainType method, _sdo_isdomachine_getdomaintype, nps.SDO_isdomachine_getdomaintype, sdo.isdomachine_getdomaintype, sdoias/ISdoMachine::GetDomainType
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
req.typenames: VENDORPROPERTIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Iassdo.dll
api_name:
-	ISdoMachine.GetDomainType
-	SdoMachine.GetDomainType
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISdoMachine::GetDomainType


## -description


The <b>GetDomainType</b> retrieves the type of domain in which the SDO computer 
    resides.


## -parameters




### -param eDomainType [out]

Pointer to an <a href="https://msdn.microsoft.com/d6c36f76-d265-446b-986e-b23d9550ba3b">IASDOMAINTYPE</a> variable that receives 
      the type of the domain in which the SDO computer resides.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Before calling this method, use the 
    <a href="https://msdn.microsoft.com/444ba670-8224-40bc-b0e4-585c682deafd">ISdoMachine::Attach</a> method to attach to the SDO 
    computer.




## -see-also




<a href="https://msdn.microsoft.com/d6c36f76-d265-446b-986e-b23d9550ba3b">IASDOMAINTYPE</a>



<a href="https://msdn.microsoft.com/11372116-56eb-4d8e-8f28-4402835ee903">ISdoMachine</a>



<a href="https://msdn.microsoft.com/444ba670-8224-40bc-b0e4-585c682deafd">ISdoMachine::Attach</a>
 

 

