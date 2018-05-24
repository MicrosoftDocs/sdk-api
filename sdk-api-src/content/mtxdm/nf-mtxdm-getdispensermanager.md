---
UID: NF:mtxdm.GetDispenserManager
title: GetDispenserManager function
author: windows-driver-content
description: Retrieves the dispenser manager's IDispenserManager interface.
old-location: cos\getdispensermanager.htm
old-project: cossdk
ms.assetid: db344236-a8be-49ec-91fd-dfcc0bd4412c
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetDispenserManager, GetDispenserManager function [COM+], _dtc_GetDispenserManager_Function, cos.getdispensermanager, mtxdm/GetDispenserManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mtxdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MTP_COMMAND_DATA_OUT, *PMTP_COMMAND_DATA_OUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	MtxDM.dll
api_name:
-	GetDispenserManager
product: Windows
targetos: Windows
req.lib: MtxDM.lib
req.dll: MtxDM.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# GetDispenserManager function


## -description


Retrieves the dispenser manager's <a href="https://msdn.microsoft.com/a0465d78-f8b7-4934-9dc6-c8f0ead04bf1">IDispenserManager</a> interface.


## -parameters




### -param Arg1

TBD




#### - ppIDispenserManager [out]

A pointer to the location that receives the <a href="https://msdn.microsoft.com/a0465d78-f8b7-4934-9dc6-c8f0ead04bf1">IDispenserManager</a> interface pointer.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/a0465d78-f8b7-4934-9dc6-c8f0ead04bf1">IDispenserManager</a>
 

 

