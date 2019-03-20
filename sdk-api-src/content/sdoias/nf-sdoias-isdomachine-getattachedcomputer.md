---
UID: NF:sdoias.ISdoMachine.GetAttachedComputer
title: ISdoMachine::GetAttachedComputer (sdoias.h)
author: windows-sdk-content
description: The GetAttachedComputer method retrieves the name of the computer that is currently attached as an SDO computer.
old-location: nps\SDO_isdomachine_getattachedcomputer.htm
tech.root: Nps
ms.assetid: ac2fe3e3-a1cb-4642-90af-2b0203e29251
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAttachedComputer, GetAttachedComputer method [Network Policy Server], GetAttachedComputer method [Network Policy Server],ISdoMachine interface, GetAttachedComputer method [Network Policy Server],SdoMachine object, ISdoMachine interface [Network Policy Server],GetAttachedComputer method, ISdoMachine.GetAttachedComputer, ISdoMachine::GetAttachedComputer, SdoMachine object [Network Policy Server],GetAttachedComputer method, _sdo_isdomachine_getattachedcomputer, nps.SDO_isdomachine_getattachedcomputer, sdo.isdomachine_getattachedcomputer, sdoias/ISdoMachine::GetAttachedComputer
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
 - ISdoMachine.GetAttachedComputer
 - SdoMachine.GetAttachedComputer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISdoMachine::GetAttachedComputer


## -description


The <b>GetAttachedComputer</b> method 
    retrieves the name of the computer that is currently attached as an SDO computer.


## -parameters




### -param bstrComputerName [out]

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms221069(v=VS.85).aspx">BSTR</a> that 
      receives the name of the computer that is the currently-attached SDO computer.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If no computer is currently attached, the return value is <b>E_FAIL</b>.

The method may also return one of the following error codes.




## -remarks



The <b>GetAttachedComputer</b> allocates 
    the memory for the <a href="https://msdn.microsoft.com/en-us/library/ms221069(v=VS.85).aspx">BSTR</a> 
    variable. The calling application should free this memory by calling 
    <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>.




## -see-also




<a href="https://msdn.microsoft.com/11372116-56eb-4d8e-8f28-4402835ee903">ISdoMachine</a>



<a href="https://msdn.microsoft.com/444ba670-8224-40bc-b0e4-585c682deafd">ISdoMachine::Attach</a>
 

 

