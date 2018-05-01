---
UID: NF:sdoias.ISdoMachine.IsDirectoryAvailable
title: ISdoMachine::IsDirectoryAvailable method
author: windows-driver-content
description: The IsDirectoryAvailable method tests whether an Active Directory service is available on the SDO computer.
old-location: nps\SDO_isdomachine_isdirectoryavailable.htm
old-project: Nps
ms.assetid: 733d2911-7e1d-4f73-ae24-1bb748213c1c
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ISdoMachine, ISdoMachine interface [Network Policy Server], IsDirectoryAvailable method, ISdoMachine::IsDirectoryAvailable, IsDirectoryAvailable method [Network Policy Server], IsDirectoryAvailable method [Network Policy Server], ISdoMachine interface, IsDirectoryAvailable method [Network Policy Server], SdoMachine object, IsDirectoryAvailable,ISdoMachine.IsDirectoryAvailable, SdoMachine object [Network Policy Server], IsDirectoryAvailable method, _sdo_isdomachine_isdirectoryavailable, nps.SDO_isdomachine_isdirectoryavailable, sdo.isdomachine_isdirectoryavailable, sdoias/ISdoMachine::IsDirectoryAvailable
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
-	ISdoMachine.IsDirectoryAvailable
-	SdoMachine.IsDirectoryAvailable
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISdoMachine::IsDirectoryAvailable method


## -description


The 
<b>IsDirectoryAvailable</b> method tests whether an Active Directory service is available on the SDO computer.


## -parameters




### -param boolDirectoryAvailable [out]

Specifies whether the Active Directory is available. If the Active Directory is available, this parameter is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Before calling this method, use the 
<a href="https://msdn.microsoft.com/444ba670-8224-40bc-b0e4-585c682deafd">ISdoMachine::Attach</a> method to attach to the SDO computer.

<div class="alert"><b>Important</b>  Always returns <b>VARIANT_FALSE</b> in the current implementation.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/11372116-56eb-4d8e-8f28-4402835ee903">ISdoMachine</a>



<a href="https://msdn.microsoft.com/444ba670-8224-40bc-b0e4-585c682deafd">ISdoMachine::Attach</a>
 

 

