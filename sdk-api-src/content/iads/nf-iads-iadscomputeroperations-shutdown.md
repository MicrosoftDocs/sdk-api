---
UID: NF:iads.IADsComputerOperations.Shutdown
title: IADsComputerOperations::Shutdown
author: windows-sdk-content
description: The IADsComputerOperations::Shutdown method causes a computer under ADSI control to execute the shutdown operation with an optional reboot.
old-location: adsi\iadscomputeroperations_shutdown.htm
tech.root: adsi
ms.assetid: b13502d6-11eb-406b-bed0-e9d14e61e424
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IADsComputerOperations interface [ADSI],Shutdown method, IADsComputerOperations.Shutdown, IADsComputerOperations::Shutdown, Shutdown, Shutdown method [ADSI], Shutdown method [ADSI],IADsComputerOperations interface, _ds_iadscomputeroperations_shutdown, adsi.iadscomputeroperations__shutdown, adsi.iadscomputeroperations_shutdown, iads/IADsComputerOperations::Shutdown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsComputerOperations.Shutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsComputerOperations::Shutdown


## -description


The <b>IADsComputerOperations::Shutdown</b> method causes a computer under ADSI control to execute the shutdown operation with an optional reboot.


## -parameters




### -param bReboot [in]

If <b>TRUE</b>, then reboot the computer after the shutdown is complete.


## -returns



This method supports the standard return values, as well as the following:

For other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/e2b90a98-5777-42c2-95dd-4623e738c4da">IADsComputer</a>



<a href="https://msdn.microsoft.com/9b0155ce-f313-43fa-8605-650aa8f38587">IADsComputerOperations</a>
 

 

