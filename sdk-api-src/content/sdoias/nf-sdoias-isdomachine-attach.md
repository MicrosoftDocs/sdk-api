---
UID: NF:sdoias.ISdoMachine.Attach
title: ISdoMachine::Attach
author: windows-sdk-content
description: The Attach method attaches to an SDO computer. Attaching to an SDO computer is the first step is using the SDO API to administer that computer.
old-location: nps\SDO_isdomachine_attach.htm
tech.root: Nps
ms.assetid: 444ba670-8224-40bc-b0e4-585c682deafd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Attach, Attach method [Network Policy Server], Attach method [Network Policy Server],ISdoMachine interface, Attach method [Network Policy Server],SdoMachine object, ISdoMachine interface [Network Policy Server],Attach method, ISdoMachine.Attach, ISdoMachine::Attach, SdoMachine object [Network Policy Server],Attach method, _sdo_isdomachine_attach, nps.SDO_isdomachine_attach, sdo.isdomachine_attach, sdoias/ISdoMachine::Attach
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
 - ISdoMachine.Attach
 - SdoMachine.Attach
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISdoMachine::Attach


## -description


The 
<b>Attach</b> method attaches to an SDO computer. Attaching to an SDO computer is the first step is using the SDO API to administer that computer.


## -parameters




### -param bstrComputerName [in]

Specifies a 
<a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> variable that contains the name of the computer to which to attach. If this parameter specifies a <b>NULL</b> string, the local computer is attached.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If a computer is already attached, the return value is <b>E_FAIL</b>.

The method may also return one of the following error codes.




## -remarks



Use the 
<a href="https://msdn.microsoft.com/ac2fe3e3-a1cb-4642-90af-2b0203e29251">ISdoMachine::GetAttachedComputer</a> method to determine if a computer is already attached.




## -see-also




<a href="https://msdn.microsoft.com/11372116-56eb-4d8e-8f28-4402835ee903">ISdoMachine</a>



<a href="https://msdn.microsoft.com/ac2fe3e3-a1cb-4642-90af-2b0203e29251">ISdoMachine::GetAttachedComputer</a>
 

 

