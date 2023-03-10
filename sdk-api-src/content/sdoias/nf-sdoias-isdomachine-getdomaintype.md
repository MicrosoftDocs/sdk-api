---
UID: NF:sdoias.ISdoMachine.GetDomainType
title: ISdoMachine::GetDomainType (sdoias.h)
description: The GetDomainType retrieves the type of domain in which the SDO computer resides.
helpviewer_keywords: ["GetDomainType","GetDomainType method [Network Policy Server]","GetDomainType method [Network Policy Server]","ISdoMachine interface","GetDomainType method [Network Policy Server]","SdoMachine object","ISdoMachine interface [Network Policy Server]","GetDomainType method","ISdoMachine.GetDomainType","ISdoMachine::GetDomainType","SdoMachine object [Network Policy Server]","GetDomainType method","_sdo_isdomachine_getdomaintype","nps.SDO_isdomachine_getdomaintype","sdo.isdomachine_getdomaintype","sdoias/ISdoMachine::GetDomainType"]
old-location: nps\SDO_isdomachine_getdomaintype.htm
tech.root: Nps
ms.assetid: 9c22ec67-4a12-4487-bac5-8f0e666b8029
ms.date: 12/05/2018
ms.keywords: GetDomainType, GetDomainType method [Network Policy Server], GetDomainType method [Network Policy Server],ISdoMachine interface, GetDomainType method [Network Policy Server],SdoMachine object, ISdoMachine interface [Network Policy Server],GetDomainType method, ISdoMachine.GetDomainType, ISdoMachine::GetDomainType, SdoMachine object [Network Policy Server],GetDomainType method, _sdo_isdomachine_getdomaintype, nps.SDO_isdomachine_getdomaintype, sdo.isdomachine_getdomaintype, sdoias/ISdoMachine::GetDomainType
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
 - ISdoMachine::GetDomainType
 - sdoias/ISdoMachine::GetDomainType
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
 - ISdoMachine.GetDomainType
 - SdoMachine.GetDomainType
---

# ISdoMachine::GetDomainType


## -description

The <b>GetDomainType</b> retrieves the type of domain in which the SDO computer 
    resides.

## -parameters

### -param eDomainType [out]

Pointer to an <a href="/windows/win32/api/sdoias/ne-sdoias-iasdomaintype">IASDOMAINTYPE</a> variable that receives 
      the type of the domain in which the SDO computer resides.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -remarks

Before calling this method, use the 
    <a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach">ISdoMachine::Attach</a> method to attach to the SDO 
    computer.

## -see-also

<a href="/windows/win32/api/sdoias/ne-sdoias-iasdomaintype">IASDOMAINTYPE</a>



<a href="/windows/desktop/api/sdoias/nn-sdoias-isdomachine">ISdoMachine</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach">ISdoMachine::Attach</a>