---
UID: NF:sdoias.ISdoMachine.GetAttachedComputer
title: ISdoMachine::GetAttachedComputer
author: windows-sdk-content
description: The GetAttachedComputer method retrieves the name of the computer that is currently attached as an SDO computer.
old-location: nps\SDO_isdomachine_getattachedcomputer.htm
old-project: Nps
ms.assetid: ac2fe3e3-a1cb-4642-90af-2b0203e29251
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetAttachedComputer, GetAttachedComputer method [Network Policy Server], GetAttachedComputer method [Network Policy Server],ISdoMachine interface, GetAttachedComputer method [Network Policy Server],SdoMachine object, ISdoMachine interface [Network Policy Server],GetAttachedComputer method, ISdoMachine.GetAttachedComputer, ISdoMachine::GetAttachedComputer, SdoMachine object [Network Policy Server],GetAttachedComputer method, _sdo_isdomachine_getattachedcomputer, nps.SDO_isdomachine_getattachedcomputer, sdo.isdomachine_getattachedcomputer, sdoias/ISdoMachine::GetAttachedComputer
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VENDORPROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoMachine.GetAttachedComputer
 - SdoMachine.GetAttachedComputer
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISdoMachine::GetAttachedComputer


## -description


The <b>GetAttachedComputer</b> method 
    retrieves the name of the computer that is currently attached as an SDO computer.


## -parameters




### -param bstrComputerName [out]

Pointer to a <a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> that 
      receives the name of the computer that is the currently-attached SDO computer.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If no computer is currently attached, the return value is <b>E_FAIL</b>.

The method may also return one of the following error codes.




## -remarks



The <b>GetAttachedComputer</b> allocates 
    the memory for the <a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> 
    variable. The calling application should free this memory by calling 
    <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>.




## -see-also




<a href="https://msdn.microsoft.com/11372116-56eb-4d8e-8f28-4402835ee903">ISdoMachine</a>



<a href="https://msdn.microsoft.com/444ba670-8224-40bc-b0e4-585c682deafd">ISdoMachine::Attach</a>
 

 

