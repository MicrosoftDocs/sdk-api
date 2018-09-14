---
UID: NF:sdoias.ISdoMachine.GetUserSDO
title: ISdoMachine::GetUserSDO
author: windows-sdk-content
description: The GetUserSDO method retrieves an interface to the Server Data Object (SDO) for the specified user.
old-location: nps\SDO_isdomachine_getusersdo.htm
tech.root: Nps
ms.assetid: c416c0db-836a-4056-bcd7-819f10923446
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetUserSDO, GetUserSDO method [Network Policy Server], GetUserSDO method [Network Policy Server],ISdoMachine interface, GetUserSDO method [Network Policy Server],SdoMachine object, ISdoMachine interface [Network Policy Server],GetUserSDO method, ISdoMachine.GetUserSDO, ISdoMachine::GetUserSDO, SdoMachine object [Network Policy Server],GetUserSDO method, _sdo_isdomachine_getusersdo, nps.SDO_isdomachine_getusersdo, sdo.isdomachine_getusersdo, sdoias/ISdoMachine::GetUserSDO
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
 - ISdoMachine.GetUserSDO
 - SdoMachine.GetUserSDO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISdoMachine::GetUserSDO


## -description


The <b>GetUserSDO</b> method retrieves an interface 
    to the Server Data Object (SDO) for the specified user.


## -parameters




### -param eDataStore [in]

Specifies a value from the <a href="https://msdn.microsoft.com/1eec69f9-b82e-48e5-a471-0a0626d91957">IASDATASTORE</a> enumeration 
      type.


### -param bstrUserName [in]

Specifies a <a href="https://msdn.microsoft.com/en-us/library/ms221069(v=VS.85).aspx">BSTR</a> that contains 
      the name of the user. The name can be in Lightweight Directory Access Protocol (LDAP) format, or in Security 
      Accounts Manager (SAM) format.


### -param ppUserSDO [out]

Pointer to a pointer that points to an <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface 
      pointer. Use the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> method of this 
      <b>IUnknown</b> interface to obtain an 
      <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface to an 
      <a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a> object for the specified user.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Before calling this method, use the 
    <a href="https://msdn.microsoft.com/444ba670-8224-40bc-b0e4-585c682deafd">ISdoMachine::Attach</a> method to attach to the SDO 
    computer.

If the SDO computer has a directory, then the 
    <b>ISdoMachine::GetUserSDO</b> automatically uses the 
    <b>DATA_STORE_DIRECTORY</b> value of 
    <a href="https://msdn.microsoft.com/1eec69f9-b82e-48e5-a471-0a0626d91957">IASDATASTORE</a> instead of 
    <b>DATA_STORE_LOCAL</b>.

None of the parameters can be <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/11372116-56eb-4d8e-8f28-4402835ee903">ISdoMachine</a>



<a href="https://msdn.microsoft.com/444ba670-8224-40bc-b0e4-585c682deafd">ISdoMachine::Attach</a>



<a href="https://msdn.microsoft.com/440628f8-081b-4e7f-bdb2-760ff9bd0d77">Retrieving a User SDO</a>



<a href="https://msdn.microsoft.com/ce16b0e4-3be1-42fc-a489-d3ddce2ebf3f">USERPROPERTIES</a>
 

 

