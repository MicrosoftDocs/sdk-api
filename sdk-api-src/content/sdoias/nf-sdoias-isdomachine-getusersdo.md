---
UID: NF:sdoias.ISdoMachine.GetUserSDO
title: ISdoMachine::GetUserSDO (sdoias.h)
description: The GetUserSDO method retrieves an interface to the Server Data Object (SDO) for the specified user.
helpviewer_keywords: ["GetUserSDO","GetUserSDO method [Network Policy Server]","GetUserSDO method [Network Policy Server]","ISdoMachine interface","GetUserSDO method [Network Policy Server]","SdoMachine object","ISdoMachine interface [Network Policy Server]","GetUserSDO method","ISdoMachine.GetUserSDO","ISdoMachine::GetUserSDO","SdoMachine object [Network Policy Server]","GetUserSDO method","_sdo_isdomachine_getusersdo","nps.SDO_isdomachine_getusersdo","sdo.isdomachine_getusersdo","sdoias/ISdoMachine::GetUserSDO"]
old-location: nps\SDO_isdomachine_getusersdo.htm
tech.root: Nps
ms.assetid: c416c0db-836a-4056-bcd7-819f10923446
ms.date: 12/05/2018
ms.keywords: GetUserSDO, GetUserSDO method [Network Policy Server], GetUserSDO method [Network Policy Server],ISdoMachine interface, GetUserSDO method [Network Policy Server],SdoMachine object, ISdoMachine interface [Network Policy Server],GetUserSDO method, ISdoMachine.GetUserSDO, ISdoMachine::GetUserSDO, SdoMachine object [Network Policy Server],GetUserSDO method, _sdo_isdomachine_getusersdo, nps.SDO_isdomachine_getusersdo, sdo.isdomachine_getusersdo, sdoias/ISdoMachine::GetUserSDO
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
 - ISdoMachine::GetUserSDO
 - sdoias/ISdoMachine::GetUserSDO
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
 - ISdoMachine.GetUserSDO
 - SdoMachine.GetUserSDO
---

# ISdoMachine::GetUserSDO


## -description

The <b>GetUserSDO</b> method retrieves an interface 
    to the Server Data Object (SDO) for the specified user.

## -parameters

### -param eDataStore [in]

Specifies a value from the <a href="/windows/desktop/api/sdoias/ne-sdoias-iasdatastore">IASDATASTORE</a> enumeration 
      type.

### -param bstrUserName [in]

Specifies a <a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> that contains 
      the name of the user. The name can be in Lightweight Directory Access Protocol (LDAP) format, or in Security 
      Accounts Manager (SAM) format.

### -param ppUserSDO [out]

Pointer to a pointer that points to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface 
      pointer. Use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of this 
      <b>IUnknown</b> interface to obtain an 
      <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface to an 
      <a href="/windows/desktop/api/sdoias/nn-sdoias-isdo">ISdo</a> object for the specified user.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -remarks

Before calling this method, use the 
    <a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach">ISdoMachine::Attach</a> method to attach to the SDO 
    computer.

If the SDO computer has a directory, then the 
    <b>ISdoMachine::GetUserSDO</b> automatically uses the 
    <b>DATA_STORE_DIRECTORY</b> value of 
    <a href="/windows/desktop/api/sdoias/ne-sdoias-iasdatastore">IASDATASTORE</a> instead of 
    <b>DATA_STORE_LOCAL</b>.

None of the parameters can be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/sdoias/nn-sdoias-isdomachine">ISdoMachine</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach">ISdoMachine::Attach</a>



<a href="/windows/desktop/Nps/sdo-retrieving-a-user-sdo">Retrieving a User SDO</a>



<a href="/windows/desktop/api/sdoias/ne-sdoias-userproperties">USERPROPERTIES</a>