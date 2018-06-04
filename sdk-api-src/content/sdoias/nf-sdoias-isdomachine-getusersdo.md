---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

Specifies a <a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> that contains 
      the name of the user. The name can be in Lightweight Directory Access Protocol (LDAP) format, or in Security 
      Accounts Manager (SAM) format.


### -param ppUserSDO [out]

Pointer to a pointer that points to an <a href="_com_iunknown">IUnknown</a> interface 
      pointer. Use the <a href="_com_iunknown_queryinterface">QueryInterface</a> method of this 
      <b>IUnknown</b> interface to obtain an 
      <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface to an 
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



<a href="https://msdn.microsoft.com/library/windows/hardware/hh973206">USERPROPERTIES</a>
 

 

